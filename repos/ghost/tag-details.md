<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.89`](#ghost589)
-	[`ghost:5.89-alpine`](#ghost589-alpine)
-	[`ghost:5.89.5`](#ghost5895)
-	[`ghost:5.89.5-alpine`](#ghost5895-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:27b2029266d5ef5f36d13e201a58cabfe75f611ca74afa0e7f693a06fa8fa692
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
$ docker pull ghost@sha256:86786e9fd3a318b1e3e047cdc6e0c86f3b89a5048a916ac5e37937811e55e9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287856892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab6d0ae7ae1809d944207c72426c01285be8a3d5d6300d30f91c571da7682fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a229b4e56f545f0831dcbf11ad1a896cda878b6fbc45114e57fcdaeaffcdc3`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42c00a0ef3813e6a0ceb58e667d811154a603255d660c9d837195a348d0b80b`  
		Last Modified: Tue, 13 Aug 2024 01:12:45 GMT  
		Size: 38.2 MB (38179073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f862ff7d95856d2b0773115c655e0b84e04dd46f83103cd3f264f8ec61e4e1a3`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 1.7 MB (1708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1326ef1e29286982806dcc11f5f4d5e8289c26030f2556d11e9c193ab45664c8`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ab289f7c2e68e2272b9a20dc7b47fce8cc4e017401fb8295cf21f1299265c`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 1.4 MB (1444700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3888defbab8e0ac28287ba3a82bbce7e1983bb9aa83e8e577b7708ee4bed511`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 10.8 MB (10842078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17351c9f41d78f46470f11f774df133f8bab7198107969ef0ec2e7532195c8b2`  
		Last Modified: Sat, 17 Aug 2024 00:59:35 GMT  
		Size: 206.6 MB (206552454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b31fb887501b4dd17c40a75b2745d5d763cbf49250c1c2d87fe79a8f3f820e`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7bb1f04f1250872649ac20f746c1caa2eac731baa6477ccd733518cee77f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b3110322466a372c955e2f12c6e28776bc809b369e16741d2c42b2f3a4faba`

```dockerfile
```

-	Layers:
	-	`sha256:55a8988909e625599a296e895e1216fdb782e55d25a19fb3985139492c37c68a`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 5.3 MB (5271310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee52f856bbbfdd89570c0f0d81ca935d05f7d0c3fedf43883fddad2a0327deee`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 29.3 KB (29267 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8d9ca7d47cbebfc2f39af16450f7e77ac6704627b7e12e49ba3a42bb9c868244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300406464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae0d38525a13ee5dd6d7680c2dad4ed529e44ff8f780f3a537d40adda1b7077`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca72af6520ab6cccdc25464c65a8886151f7eb3d3a68e4343ffdf07091bd15ce`  
		Last Modified: Tue, 13 Aug 2024 12:11:23 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90c93a4630f341b7911be4328e41219dc2e76bad885dcd9d182fe5aa1f1429`  
		Last Modified: Tue, 13 Aug 2024 12:22:38 GMT  
		Size: 34.8 MB (34834276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66955684eb5d036fd9e9b8474e766ec45fae24ce6fb3bff5487954a54ef50b85`  
		Last Modified: Tue, 13 Aug 2024 12:22:37 GMT  
		Size: 1.7 MB (1708463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ae18a246047f8d8ecd4bb4233dd7c39ed15da3b8bbea336431487f4acca51b`  
		Last Modified: Tue, 13 Aug 2024 12:22:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee59bc43dd129fb9bde542e4dada2b6259f095881d22a027c93fdc9fa40c00f`  
		Last Modified: Wed, 14 Aug 2024 03:00:20 GMT  
		Size: 1.4 MB (1412523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd9aaf39418c7f326bf1239ea91620f12752037ed7e554e3a59da45f119be1e`  
		Last Modified: Wed, 14 Aug 2024 03:00:21 GMT  
		Size: 10.8 MB (10840413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a560f52061cc80aeaaf5b7f84af8b106b83635c37c41ae0e2bc8ff313348f4e4`  
		Last Modified: Sat, 17 Aug 2024 01:48:50 GMT  
		Size: 226.9 MB (226888319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529c220b1a13ab629f9cf5dd611931720a14bedd2706e7268cbd9390937d559`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:20bbe2301d85efc17cba1d50f0a64d3999847375aef6e0a1475fd9eb144b4d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6afe9b6590324bf389faf2defed6e81d0f46214583ba877d2251c80df79e8a0`

```dockerfile
```

-	Layers:
	-	`sha256:b7f8bfc89f44af440cc1fec387e31397a22c7d14b1be282dd5aa293b910ab743`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 5.3 MB (5276673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5453e31a8a23b9dfa3a466c1fef976c6b287c3d12d73b0b1f36a0e8750707c71`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 29.4 KB (29405 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f2b4f0aab8ade41346601936a2f79349c122b42ef67c9c5a6e27b486ffab2f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288823816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e00ebac3611e8a35e03dc526f13c2ad2d0a5b0a7818b88f47d2cf8416a36b9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f5aecbd9ca490d421ea755047a15006ca127eb80f50d917b9b7ea9a00327f`  
		Last Modified: Tue, 13 Aug 2024 07:45:15 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1472ebe15cf68957d51ffd887cab0b99d25048f78fa7c327f016cfa940e9b0b`  
		Last Modified: Tue, 13 Aug 2024 07:49:19 GMT  
		Size: 38.2 MB (38223538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c47224750647d76572fb2d716ce23438d387b48354c1c1e02c684d67b6a77cb`  
		Last Modified: Tue, 13 Aug 2024 07:49:19 GMT  
		Size: 1.7 MB (1708240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9535a7db32f846d51a8e37c90c4d2f11bbe9c89a128d060aa7fbc210bdbd5d38`  
		Last Modified: Tue, 13 Aug 2024 07:49:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ab6a798ab76d3e208b95993058b9ef3d31dcdaa47c3c58606382342407279`  
		Last Modified: Tue, 13 Aug 2024 20:18:42 GMT  
		Size: 1.4 MB (1376502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6e7f548cfc5e04a68b39799eb888da995ea3d3ec6a38279ccb26a769fc7c37`  
		Last Modified: Tue, 13 Aug 2024 20:18:42 GMT  
		Size: 10.8 MB (10841798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3659d795ce52c30687b8a407b818d44caa13d8b8b031aa952b292a5a43f277dd`  
		Last Modified: Sat, 17 Aug 2024 01:56:24 GMT  
		Size: 207.5 MB (207512879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3405fa6bdb88b697f2eadb93bbc91ce0f1a41e8341529a3075754d703b5d6a8`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:24dd03632d1011a33ec32229a0fcc467b08e5192942ae681dcf4fd1ec03084aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679c70dc47f230134e6941a25bfa766b0eed89b463a9481b1ff2ab9a8fb6001`

```dockerfile
```

-	Layers:
	-	`sha256:525dc5bc5e77f770153d52d1a6002dfe8d0a535cadb04ab86ad07849ce48732f`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 5.3 MB (5271560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f7a753fb10f94c4ad8307eacd1fd1cf32b4ab56be113ac1a9839e27c2c2fd3`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:330f51f67333f7e144e27d22c378ff4d69ddbe9853836d46dadae44b38440520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301390889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b364fc36d159226c4a9e8872bc0512514289485114bd796e3ff5f1b4f1da93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5d8671d229877e86fab6fbbd80fd27eb274b2e69afefcdfd5ce4275304f103`  
		Last Modified: Tue, 13 Aug 2024 07:18:23 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c61ee5c081a173a619d65a0dd7744322fb2b4f174d5982d841d6e8e548c65a`  
		Last Modified: Tue, 13 Aug 2024 07:25:28 GMT  
		Size: 40.3 MB (40263153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b58dcbd8199492954fcf3b474b6a13a98f571d8ff1daafb001a22802d65f948`  
		Last Modified: Tue, 13 Aug 2024 07:25:23 GMT  
		Size: 1.7 MB (1708394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10b147a72719064981da776661a474b2fc3198427bc803662c7e67ed4d8d65e`  
		Last Modified: Tue, 13 Aug 2024 07:25:22 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574890800ac29a91e7db6120f8b2fd2cd1d50aa450e726ef69a0d71ff61db677`  
		Last Modified: Tue, 13 Aug 2024 22:39:31 GMT  
		Size: 1.4 MB (1366626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf9db1cac32d5705261307f7420e0e0e51837c368172bc69b43ee2ba024b5b0`  
		Last Modified: Tue, 13 Aug 2024 22:39:31 GMT  
		Size: 10.8 MB (10840074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9249d5d8a8decf1600cc9eff1abd23d76bc59adb762b4a6b42bb4281c8ae70`  
		Last Modified: Sat, 17 Aug 2024 03:55:53 GMT  
		Size: 214.1 MB (214086010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eb9a4284c7a1945456a7a30881f0cbbf74709696a9032e47ecec92e236ed46`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:67e3ce798f6e71cce1a6b6070523ae64a7cf9daf9396d7355bda43318c68c090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413b85452caae755fd4da6803d89334e69a3a3f85cf2782d9eb8765f776159de`

```dockerfile
```

-	Layers:
	-	`sha256:491069186e918e9dee07687c1d878e80887c143430b6a8687e792fc3a88d4506`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 5.3 MB (5268206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de62f7295637aacd421f58f7cccaa25106939a85af615df0eaba82fe35ad4fc7`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 29.4 KB (29351 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:ef7bf2caa8d2bafaac50412ab160b55c7c3e8cf39c3dea8ae8a90e6225967d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293929008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebe13ade283f37cf0057faa641308a5fe6e7537e5c77c48274c2114d89c16fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e5af7951f31ebaf8f18c4c3376d0d0bfdfd054ba6458d447fa7553077201d9`  
		Last Modified: Tue, 13 Aug 2024 05:41:02 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8085eb5c05d7c778cf29d785e9c38a9745b75f27046ccfe042db2bb8867cea4`  
		Last Modified: Tue, 13 Aug 2024 05:45:46 GMT  
		Size: 38.4 MB (38403871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1770d19b5d24606d5de2201575fcbf046e4f4b9fdd1bcfcde321bffde569fd`  
		Last Modified: Tue, 13 Aug 2024 05:45:45 GMT  
		Size: 1.7 MB (1708142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5376f828cedb7c818dfa096f2b13c0798666f7343cda359f0e775321ef59b2`  
		Last Modified: Tue, 13 Aug 2024 05:45:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb1204457289986dce2001365927b5dc939a5d8f15a43bb5f2c51a6c60f06f5`  
		Last Modified: Tue, 13 Aug 2024 21:45:58 GMT  
		Size: 1.4 MB (1410231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bf7ad47adf940e4597085675e78fcc6d423a3cbbcab8d91bcbff90fed70309`  
		Last Modified: Tue, 13 Aug 2024 21:45:58 GMT  
		Size: 10.8 MB (10844553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfca19625014dca23d4d300f9ef42f52d3bd29dfd3547596749c1127e163e52f`  
		Last Modified: Sat, 17 Aug 2024 01:08:13 GMT  
		Size: 214.1 MB (214067783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8160d53e7bfbdacb3e2f43e2cba14d82cf553b61376087ae61eb27bac17311`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:1d62252aff02d86a08ade55028b346859b8e0cde452e593b04ec3d6de2cb82a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9367dfbdc308d1a4ce9df061c32776d1e75fc2587092d8286f3c821e5cf63d`

```dockerfile
```

-	Layers:
	-	`sha256:752919c41d6d947fcaa762b7c3c5112a03c49c8063f90ac81af429d78ab587de`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 5.3 MB (5263786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82fdae27c16cf8a0b94d324d66715195ce2279cb821e31f651ebe4309de4212`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 29.3 KB (29303 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:f9040f7b37636913dbcef816cef85223291f8805e1ce851dc0b3c001c6c84680
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
$ docker pull ghost@sha256:54dfa033303e4dbb83151d411d5f4629baeacecbe903dc40c7c539b833181be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261111640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d125830a91574e240dd7863a418c0951b1a501587335cb83ecdd4617857792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfd1a7f5d0b2ad6106b6097bf76f56d3a8c3bcc5cf7fa1f5d0a0ca9dc32cbc`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 39.8 MB (39831284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f16a148263d04e03d25d24411a9a48c71d7e31131900f4110b45b53c5a23ec`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.4 MB (1382231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30aa900b096c1999e57347eefc256ac6d0f228a2427efa4b8d9b2ec9152e74`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2858d9f271023c9c88bcd4e71bf3fe06371e91388edc3e3cc07bdb39011df35`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 776.0 KB (776022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d154c0ae41efc373dab0cc6e8f963ecd2997083bf297c49fdd87b6a529ce6ebe`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 1.1 MB (1121672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bfd53e00cac2e59a3ab7bbaccb72aebf710d112e2b0e513c4d2adcec7042e2`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97566d0aa7f0342ae696f178eff7c5a27b6fc691e8cc670d7199b58809ede67f`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 10.8 MB (10842758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77173a32cbd16d9f3ddb316667631dafd2077dd5dcacf359966955c4ab748aa1`  
		Last Modified: Sat, 17 Aug 2024 00:59:18 GMT  
		Size: 203.7 MB (203737436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce50ca1cfee8a0995eea27e0454f184d778b27d80536584f0c3483dd6872be`  
		Last Modified: Sat, 17 Aug 2024 00:59:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:60d341e0d921010c73032fa63d335cbe0333ea8182ff9538d39fe5ff4aca4054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c6154fbee2f94b3793ebfeeb61c8f8ee2d106890dce278b55eda473004a9d4`

```dockerfile
```

-	Layers:
	-	`sha256:c0d34ac0732e4e908bce7848d5066d1915d87ab4740fafc5a0b28f1c79b80a3b`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 3.2 MB (3173577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b23173063df968dbcfade140449c8feaa62b687db75e6c006a309b9272d323`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 32.2 KB (32209 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:c2ac48262e1e735256e521b33ab4fe649858d671d0848c4d564f93697c3f4627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267849352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3e97dab5b29f53baec80515621bb3069feaa416f2e9d429fd5cd17c3a33489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31faeeb6568eb2da580663e85950ac0b00527da619bb2537ca4c06db51033c4b`  
		Last Modified: Tue, 23 Jul 2024 06:49:05 GMT  
		Size: 38.4 MB (38420236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3154e981db5c13ed905e8758cb01a65392f9a0fddec17cb0a5268c79c00a`  
		Last Modified: Tue, 23 Jul 2024 06:49:04 GMT  
		Size: 1.4 MB (1382242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d710ca75bd1b5c7448f0a5ae0ffe77eb30e3e18cbced8b2a3ac61359a20681`  
		Last Modified: Tue, 23 Jul 2024 06:49:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc97a7763d1ad9c4a6eb0eb073cabd71f82b6fbac5041c3fec7aad67ce7888`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 767.9 KB (767855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd0e71658dc455588dbf848c8aa8213278ed6d6762bb7d0a95d3a1e21b33f0`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 1.1 MB (1088933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaf43e4ac986fa2c0872fd605e5ec1b9a11a57160507b9d6311fd11ec709a6f`  
		Last Modified: Mon, 05 Aug 2024 19:16:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f8a66abc1a25f2f9c81a6a11661fd8419453dbce4a410d347fad6401a6545`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 10.8 MB (10846335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25110d1a7b4a9a04ffec166ae497a3f95d9b9c88d87076481003f9ae6c953ba`  
		Last Modified: Sat, 17 Aug 2024 01:10:31 GMT  
		Size: 212.2 MB (212166888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792f689c4c7be57268305e55913fbd4d250863890ea99baa50746d5dc045bc88`  
		Last Modified: Sat, 17 Aug 2024 01:10:26 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:57abebea6fd33f63a400ec51d695505a58bb9a0421fbf6384a0e25758cf0f30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479b5d7d7d947b47bd50661f8607eaf67d35ae091311c0c824fb13657f2cf206`

```dockerfile
```

-	Layers:
	-	`sha256:13ef19686b52e27c843077e3cef297965e819c769e92e60540c730f4ec92cf59`  
		Last Modified: Sat, 17 Aug 2024 01:10:26 GMT  
		Size: 32.2 KB (32167 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1fd66d20684c5f7f7434e913a7c2b44f12166b2109b8245052b421c8d40ce414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266711115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5bafeec7942643428bd4ef8cf516675d2c840174e77e68d989a96da64a9ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f2aa85ba2de2b0a8671453c081dfb01400a67eb450d92f7bdde7805dab7d7f`  
		Last Modified: Tue, 23 Jul 2024 22:47:20 GMT  
		Size: 37.9 MB (37925178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380053b85efdf6375556fb6ed33dec58dab9f4b7864d30293edee2fe6e0f456b`  
		Last Modified: Tue, 23 Jul 2024 22:47:18 GMT  
		Size: 1.4 MB (1382243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a63c1dd0e066a189a6d24ee97b01453bad055bd325dcb882486d19eac11442`  
		Last Modified: Tue, 23 Jul 2024 22:47:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d3c66ca4e9316e52e59fadb69681c1aa7087bd2f9c197572dbdea20151ee78`  
		Last Modified: Wed, 24 Jul 2024 19:11:59 GMT  
		Size: 701.1 KB (701145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f09c6c5057a81da4bef6bfebde1bda2b8dfeb070a4198bcf115bbf03609d3`  
		Last Modified: Wed, 24 Jul 2024 19:11:59 GMT  
		Size: 1.1 MB (1088903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8668f5ac081c64a3e94ef25a7099299b8c991c1c8135c426ab21170d96c56`  
		Last Modified: Wed, 24 Jul 2024 19:11:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236031c27bb799c6f89ff2895432cce7b0e78e0dd83a2b5dffb1eb79180ff5dc`  
		Last Modified: Fri, 02 Aug 2024 00:36:15 GMT  
		Size: 10.8 MB (10841015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6a9571b854d42cdfbd8288ab7e88da5ec1df3650f7c11423f63c28015f78df`  
		Last Modified: Sat, 17 Aug 2024 01:59:43 GMT  
		Size: 211.8 MB (211844336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c339d9102799ebcfd86c78d66f65cc3207be2aedae173d18816988673f5b88a1`  
		Last Modified: Sat, 17 Aug 2024 01:59:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:21bb289fd3ab2237be0555958a46983b9ea817e10344522faa07c770d501de00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3198638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b53daf498e887c251befc7d43d87b6fbd226dc1ea1c312128efecf4d567cac`

```dockerfile
```

-	Layers:
	-	`sha256:9c569031e25d13c1c913393eda3be59341b14afb6475fe68f3205e7f6c3bdf96`  
		Last Modified: Sat, 17 Aug 2024 01:59:38 GMT  
		Size: 3.2 MB (3166252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e79c8a4b1d0f5c5af7f01c293a8d4183e8d6ac054b27ffe36159237cbb581e`  
		Last Modified: Sat, 17 Aug 2024 01:59:37 GMT  
		Size: 32.4 KB (32386 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:5ecb3205a373d8b3512d001e38b6d8f7eb5cbef572504cd5abfae4f03ebcf995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280777122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb302706c55291252d0d220b9d87ae22eaff8d096c5b2d7327f1987e73aa61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34fa575f3bac771ddb2aa598addd06eb8ee9021b249cbc0e60e5e9cd74885c`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 39.5 MB (39537820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ada097bad821da4edbdb4753ce1e3ca5ddf992a4bac4a2f723b4819ac2d96`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae55db9b5c5d4ef1702f1307c5604009843d2a03b7e3b4d1e671c0d3c95abf7`  
		Last Modified: Tue, 23 Jul 2024 21:29:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ed4eb688ce66b6712e8eb220e8a4f89814f673bb18755639d9b7b8046cca6`  
		Last Modified: Mon, 29 Jul 2024 15:02:04 GMT  
		Size: 852.8 KB (852771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aa3aa3c270f53227c94ac9f82f26be4cbe7ec5ec782011ef6e251ff3721633`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 1.1 MB (1053461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a9bb8833c4ee37b000b759ab55837ac009c53dee21316aadb348c7adde940`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9d88007be0ca432c6ceea4d60d14ce107db6cadd491c3092996f44407a9be`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 10.8 MB (10841725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f79c9540bac61a07eb070eab5cc2fdf86a86aa02529d84e1ced0ce6a0a473`  
		Last Modified: Sat, 17 Aug 2024 02:08:33 GMT  
		Size: 223.7 MB (223749457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff17ffdf21532d85f407d283c912715c58cc395bf8076465838a181393f1b2`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:45ed2a7d50fc18a0908a026e3c6d14db2ccdaecbdc94a7b5c6e57cb46e478c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a002c6c6b9caa196726a92f041cd11920ce4fae685212b86c9e5295ce002799`

```dockerfile
```

-	Layers:
	-	`sha256:feb498a45b5b54519fa9a472ad837b50abc9bdcad8ae1498547b49e38366638a`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 3.2 MB (3173633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19c5012399cea1277e97804afc4a9a85ca8791966ee7ff123976998df0d1e960`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 32.6 KB (32642 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.89`

```console
$ docker pull ghost@sha256:27b2029266d5ef5f36d13e201a58cabfe75f611ca74afa0e7f693a06fa8fa692
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

### `ghost:5.89` - linux; amd64

```console
$ docker pull ghost@sha256:86786e9fd3a318b1e3e047cdc6e0c86f3b89a5048a916ac5e37937811e55e9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287856892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab6d0ae7ae1809d944207c72426c01285be8a3d5d6300d30f91c571da7682fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a229b4e56f545f0831dcbf11ad1a896cda878b6fbc45114e57fcdaeaffcdc3`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42c00a0ef3813e6a0ceb58e667d811154a603255d660c9d837195a348d0b80b`  
		Last Modified: Tue, 13 Aug 2024 01:12:45 GMT  
		Size: 38.2 MB (38179073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f862ff7d95856d2b0773115c655e0b84e04dd46f83103cd3f264f8ec61e4e1a3`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 1.7 MB (1708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1326ef1e29286982806dcc11f5f4d5e8289c26030f2556d11e9c193ab45664c8`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ab289f7c2e68e2272b9a20dc7b47fce8cc4e017401fb8295cf21f1299265c`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 1.4 MB (1444700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3888defbab8e0ac28287ba3a82bbce7e1983bb9aa83e8e577b7708ee4bed511`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 10.8 MB (10842078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17351c9f41d78f46470f11f774df133f8bab7198107969ef0ec2e7532195c8b2`  
		Last Modified: Sat, 17 Aug 2024 00:59:35 GMT  
		Size: 206.6 MB (206552454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b31fb887501b4dd17c40a75b2745d5d763cbf49250c1c2d87fe79a8f3f820e`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7bb1f04f1250872649ac20f746c1caa2eac731baa6477ccd733518cee77f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b3110322466a372c955e2f12c6e28776bc809b369e16741d2c42b2f3a4faba`

```dockerfile
```

-	Layers:
	-	`sha256:55a8988909e625599a296e895e1216fdb782e55d25a19fb3985139492c37c68a`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 5.3 MB (5271310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee52f856bbbfdd89570c0f0d81ca935d05f7d0c3fedf43883fddad2a0327deee`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 29.3 KB (29267 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8d9ca7d47cbebfc2f39af16450f7e77ac6704627b7e12e49ba3a42bb9c868244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300406464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae0d38525a13ee5dd6d7680c2dad4ed529e44ff8f780f3a537d40adda1b7077`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca72af6520ab6cccdc25464c65a8886151f7eb3d3a68e4343ffdf07091bd15ce`  
		Last Modified: Tue, 13 Aug 2024 12:11:23 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90c93a4630f341b7911be4328e41219dc2e76bad885dcd9d182fe5aa1f1429`  
		Last Modified: Tue, 13 Aug 2024 12:22:38 GMT  
		Size: 34.8 MB (34834276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66955684eb5d036fd9e9b8474e766ec45fae24ce6fb3bff5487954a54ef50b85`  
		Last Modified: Tue, 13 Aug 2024 12:22:37 GMT  
		Size: 1.7 MB (1708463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ae18a246047f8d8ecd4bb4233dd7c39ed15da3b8bbea336431487f4acca51b`  
		Last Modified: Tue, 13 Aug 2024 12:22:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee59bc43dd129fb9bde542e4dada2b6259f095881d22a027c93fdc9fa40c00f`  
		Last Modified: Wed, 14 Aug 2024 03:00:20 GMT  
		Size: 1.4 MB (1412523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd9aaf39418c7f326bf1239ea91620f12752037ed7e554e3a59da45f119be1e`  
		Last Modified: Wed, 14 Aug 2024 03:00:21 GMT  
		Size: 10.8 MB (10840413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a560f52061cc80aeaaf5b7f84af8b106b83635c37c41ae0e2bc8ff313348f4e4`  
		Last Modified: Sat, 17 Aug 2024 01:48:50 GMT  
		Size: 226.9 MB (226888319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529c220b1a13ab629f9cf5dd611931720a14bedd2706e7268cbd9390937d559`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89` - unknown; unknown

```console
$ docker pull ghost@sha256:20bbe2301d85efc17cba1d50f0a64d3999847375aef6e0a1475fd9eb144b4d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6afe9b6590324bf389faf2defed6e81d0f46214583ba877d2251c80df79e8a0`

```dockerfile
```

-	Layers:
	-	`sha256:b7f8bfc89f44af440cc1fec387e31397a22c7d14b1be282dd5aa293b910ab743`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 5.3 MB (5276673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5453e31a8a23b9dfa3a466c1fef976c6b287c3d12d73b0b1f36a0e8750707c71`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 29.4 KB (29405 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f2b4f0aab8ade41346601936a2f79349c122b42ef67c9c5a6e27b486ffab2f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288823816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e00ebac3611e8a35e03dc526f13c2ad2d0a5b0a7818b88f47d2cf8416a36b9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f5aecbd9ca490d421ea755047a15006ca127eb80f50d917b9b7ea9a00327f`  
		Last Modified: Tue, 13 Aug 2024 07:45:15 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1472ebe15cf68957d51ffd887cab0b99d25048f78fa7c327f016cfa940e9b0b`  
		Last Modified: Tue, 13 Aug 2024 07:49:19 GMT  
		Size: 38.2 MB (38223538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c47224750647d76572fb2d716ce23438d387b48354c1c1e02c684d67b6a77cb`  
		Last Modified: Tue, 13 Aug 2024 07:49:19 GMT  
		Size: 1.7 MB (1708240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9535a7db32f846d51a8e37c90c4d2f11bbe9c89a128d060aa7fbc210bdbd5d38`  
		Last Modified: Tue, 13 Aug 2024 07:49:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ab6a798ab76d3e208b95993058b9ef3d31dcdaa47c3c58606382342407279`  
		Last Modified: Tue, 13 Aug 2024 20:18:42 GMT  
		Size: 1.4 MB (1376502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6e7f548cfc5e04a68b39799eb888da995ea3d3ec6a38279ccb26a769fc7c37`  
		Last Modified: Tue, 13 Aug 2024 20:18:42 GMT  
		Size: 10.8 MB (10841798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3659d795ce52c30687b8a407b818d44caa13d8b8b031aa952b292a5a43f277dd`  
		Last Modified: Sat, 17 Aug 2024 01:56:24 GMT  
		Size: 207.5 MB (207512879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3405fa6bdb88b697f2eadb93bbc91ce0f1a41e8341529a3075754d703b5d6a8`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89` - unknown; unknown

```console
$ docker pull ghost@sha256:24dd03632d1011a33ec32229a0fcc467b08e5192942ae681dcf4fd1ec03084aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679c70dc47f230134e6941a25bfa766b0eed89b463a9481b1ff2ab9a8fb6001`

```dockerfile
```

-	Layers:
	-	`sha256:525dc5bc5e77f770153d52d1a6002dfe8d0a535cadb04ab86ad07849ce48732f`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 5.3 MB (5271560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f7a753fb10f94c4ad8307eacd1fd1cf32b4ab56be113ac1a9839e27c2c2fd3`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89` - linux; ppc64le

```console
$ docker pull ghost@sha256:330f51f67333f7e144e27d22c378ff4d69ddbe9853836d46dadae44b38440520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301390889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b364fc36d159226c4a9e8872bc0512514289485114bd796e3ff5f1b4f1da93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5d8671d229877e86fab6fbbd80fd27eb274b2e69afefcdfd5ce4275304f103`  
		Last Modified: Tue, 13 Aug 2024 07:18:23 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c61ee5c081a173a619d65a0dd7744322fb2b4f174d5982d841d6e8e548c65a`  
		Last Modified: Tue, 13 Aug 2024 07:25:28 GMT  
		Size: 40.3 MB (40263153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b58dcbd8199492954fcf3b474b6a13a98f571d8ff1daafb001a22802d65f948`  
		Last Modified: Tue, 13 Aug 2024 07:25:23 GMT  
		Size: 1.7 MB (1708394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10b147a72719064981da776661a474b2fc3198427bc803662c7e67ed4d8d65e`  
		Last Modified: Tue, 13 Aug 2024 07:25:22 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574890800ac29a91e7db6120f8b2fd2cd1d50aa450e726ef69a0d71ff61db677`  
		Last Modified: Tue, 13 Aug 2024 22:39:31 GMT  
		Size: 1.4 MB (1366626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf9db1cac32d5705261307f7420e0e0e51837c368172bc69b43ee2ba024b5b0`  
		Last Modified: Tue, 13 Aug 2024 22:39:31 GMT  
		Size: 10.8 MB (10840074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9249d5d8a8decf1600cc9eff1abd23d76bc59adb762b4a6b42bb4281c8ae70`  
		Last Modified: Sat, 17 Aug 2024 03:55:53 GMT  
		Size: 214.1 MB (214086010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eb9a4284c7a1945456a7a30881f0cbbf74709696a9032e47ecec92e236ed46`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89` - unknown; unknown

```console
$ docker pull ghost@sha256:67e3ce798f6e71cce1a6b6070523ae64a7cf9daf9396d7355bda43318c68c090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413b85452caae755fd4da6803d89334e69a3a3f85cf2782d9eb8765f776159de`

```dockerfile
```

-	Layers:
	-	`sha256:491069186e918e9dee07687c1d878e80887c143430b6a8687e792fc3a88d4506`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 5.3 MB (5268206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de62f7295637aacd421f58f7cccaa25106939a85af615df0eaba82fe35ad4fc7`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 29.4 KB (29351 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89` - linux; s390x

```console
$ docker pull ghost@sha256:ef7bf2caa8d2bafaac50412ab160b55c7c3e8cf39c3dea8ae8a90e6225967d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293929008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebe13ade283f37cf0057faa641308a5fe6e7537e5c77c48274c2114d89c16fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e5af7951f31ebaf8f18c4c3376d0d0bfdfd054ba6458d447fa7553077201d9`  
		Last Modified: Tue, 13 Aug 2024 05:41:02 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8085eb5c05d7c778cf29d785e9c38a9745b75f27046ccfe042db2bb8867cea4`  
		Last Modified: Tue, 13 Aug 2024 05:45:46 GMT  
		Size: 38.4 MB (38403871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1770d19b5d24606d5de2201575fcbf046e4f4b9fdd1bcfcde321bffde569fd`  
		Last Modified: Tue, 13 Aug 2024 05:45:45 GMT  
		Size: 1.7 MB (1708142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5376f828cedb7c818dfa096f2b13c0798666f7343cda359f0e775321ef59b2`  
		Last Modified: Tue, 13 Aug 2024 05:45:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb1204457289986dce2001365927b5dc939a5d8f15a43bb5f2c51a6c60f06f5`  
		Last Modified: Tue, 13 Aug 2024 21:45:58 GMT  
		Size: 1.4 MB (1410231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bf7ad47adf940e4597085675e78fcc6d423a3cbbcab8d91bcbff90fed70309`  
		Last Modified: Tue, 13 Aug 2024 21:45:58 GMT  
		Size: 10.8 MB (10844553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfca19625014dca23d4d300f9ef42f52d3bd29dfd3547596749c1127e163e52f`  
		Last Modified: Sat, 17 Aug 2024 01:08:13 GMT  
		Size: 214.1 MB (214067783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8160d53e7bfbdacb3e2f43e2cba14d82cf553b61376087ae61eb27bac17311`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89` - unknown; unknown

```console
$ docker pull ghost@sha256:1d62252aff02d86a08ade55028b346859b8e0cde452e593b04ec3d6de2cb82a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9367dfbdc308d1a4ce9df061c32776d1e75fc2587092d8286f3c821e5cf63d`

```dockerfile
```

-	Layers:
	-	`sha256:752919c41d6d947fcaa762b7c3c5112a03c49c8063f90ac81af429d78ab587de`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 5.3 MB (5263786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82fdae27c16cf8a0b94d324d66715195ce2279cb821e31f651ebe4309de4212`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 29.3 KB (29303 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.89-alpine`

```console
$ docker pull ghost@sha256:f9040f7b37636913dbcef816cef85223291f8805e1ce851dc0b3c001c6c84680
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

### `ghost:5.89-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:54dfa033303e4dbb83151d411d5f4629baeacecbe903dc40c7c539b833181be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261111640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d125830a91574e240dd7863a418c0951b1a501587335cb83ecdd4617857792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfd1a7f5d0b2ad6106b6097bf76f56d3a8c3bcc5cf7fa1f5d0a0ca9dc32cbc`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 39.8 MB (39831284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f16a148263d04e03d25d24411a9a48c71d7e31131900f4110b45b53c5a23ec`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.4 MB (1382231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30aa900b096c1999e57347eefc256ac6d0f228a2427efa4b8d9b2ec9152e74`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2858d9f271023c9c88bcd4e71bf3fe06371e91388edc3e3cc07bdb39011df35`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 776.0 KB (776022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d154c0ae41efc373dab0cc6e8f963ecd2997083bf297c49fdd87b6a529ce6ebe`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 1.1 MB (1121672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bfd53e00cac2e59a3ab7bbaccb72aebf710d112e2b0e513c4d2adcec7042e2`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97566d0aa7f0342ae696f178eff7c5a27b6fc691e8cc670d7199b58809ede67f`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 10.8 MB (10842758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77173a32cbd16d9f3ddb316667631dafd2077dd5dcacf359966955c4ab748aa1`  
		Last Modified: Sat, 17 Aug 2024 00:59:18 GMT  
		Size: 203.7 MB (203737436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce50ca1cfee8a0995eea27e0454f184d778b27d80536584f0c3483dd6872be`  
		Last Modified: Sat, 17 Aug 2024 00:59:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:60d341e0d921010c73032fa63d335cbe0333ea8182ff9538d39fe5ff4aca4054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c6154fbee2f94b3793ebfeeb61c8f8ee2d106890dce278b55eda473004a9d4`

```dockerfile
```

-	Layers:
	-	`sha256:c0d34ac0732e4e908bce7848d5066d1915d87ab4740fafc5a0b28f1c79b80a3b`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 3.2 MB (3173577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b23173063df968dbcfade140449c8feaa62b687db75e6c006a309b9272d323`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 32.2 KB (32209 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:c2ac48262e1e735256e521b33ab4fe649858d671d0848c4d564f93697c3f4627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267849352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3e97dab5b29f53baec80515621bb3069feaa416f2e9d429fd5cd17c3a33489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31faeeb6568eb2da580663e85950ac0b00527da619bb2537ca4c06db51033c4b`  
		Last Modified: Tue, 23 Jul 2024 06:49:05 GMT  
		Size: 38.4 MB (38420236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3154e981db5c13ed905e8758cb01a65392f9a0fddec17cb0a5268c79c00a`  
		Last Modified: Tue, 23 Jul 2024 06:49:04 GMT  
		Size: 1.4 MB (1382242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d710ca75bd1b5c7448f0a5ae0ffe77eb30e3e18cbced8b2a3ac61359a20681`  
		Last Modified: Tue, 23 Jul 2024 06:49:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc97a7763d1ad9c4a6eb0eb073cabd71f82b6fbac5041c3fec7aad67ce7888`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 767.9 KB (767855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd0e71658dc455588dbf848c8aa8213278ed6d6762bb7d0a95d3a1e21b33f0`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 1.1 MB (1088933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaf43e4ac986fa2c0872fd605e5ec1b9a11a57160507b9d6311fd11ec709a6f`  
		Last Modified: Mon, 05 Aug 2024 19:16:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f8a66abc1a25f2f9c81a6a11661fd8419453dbce4a410d347fad6401a6545`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 10.8 MB (10846335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25110d1a7b4a9a04ffec166ae497a3f95d9b9c88d87076481003f9ae6c953ba`  
		Last Modified: Sat, 17 Aug 2024 01:10:31 GMT  
		Size: 212.2 MB (212166888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792f689c4c7be57268305e55913fbd4d250863890ea99baa50746d5dc045bc88`  
		Last Modified: Sat, 17 Aug 2024 01:10:26 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:57abebea6fd33f63a400ec51d695505a58bb9a0421fbf6384a0e25758cf0f30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479b5d7d7d947b47bd50661f8607eaf67d35ae091311c0c824fb13657f2cf206`

```dockerfile
```

-	Layers:
	-	`sha256:13ef19686b52e27c843077e3cef297965e819c769e92e60540c730f4ec92cf59`  
		Last Modified: Sat, 17 Aug 2024 01:10:26 GMT  
		Size: 32.2 KB (32167 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1fd66d20684c5f7f7434e913a7c2b44f12166b2109b8245052b421c8d40ce414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266711115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5bafeec7942643428bd4ef8cf516675d2c840174e77e68d989a96da64a9ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f2aa85ba2de2b0a8671453c081dfb01400a67eb450d92f7bdde7805dab7d7f`  
		Last Modified: Tue, 23 Jul 2024 22:47:20 GMT  
		Size: 37.9 MB (37925178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380053b85efdf6375556fb6ed33dec58dab9f4b7864d30293edee2fe6e0f456b`  
		Last Modified: Tue, 23 Jul 2024 22:47:18 GMT  
		Size: 1.4 MB (1382243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a63c1dd0e066a189a6d24ee97b01453bad055bd325dcb882486d19eac11442`  
		Last Modified: Tue, 23 Jul 2024 22:47:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d3c66ca4e9316e52e59fadb69681c1aa7087bd2f9c197572dbdea20151ee78`  
		Last Modified: Wed, 24 Jul 2024 19:11:59 GMT  
		Size: 701.1 KB (701145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f09c6c5057a81da4bef6bfebde1bda2b8dfeb070a4198bcf115bbf03609d3`  
		Last Modified: Wed, 24 Jul 2024 19:11:59 GMT  
		Size: 1.1 MB (1088903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8668f5ac081c64a3e94ef25a7099299b8c991c1c8135c426ab21170d96c56`  
		Last Modified: Wed, 24 Jul 2024 19:11:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236031c27bb799c6f89ff2895432cce7b0e78e0dd83a2b5dffb1eb79180ff5dc`  
		Last Modified: Fri, 02 Aug 2024 00:36:15 GMT  
		Size: 10.8 MB (10841015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6a9571b854d42cdfbd8288ab7e88da5ec1df3650f7c11423f63c28015f78df`  
		Last Modified: Sat, 17 Aug 2024 01:59:43 GMT  
		Size: 211.8 MB (211844336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c339d9102799ebcfd86c78d66f65cc3207be2aedae173d18816988673f5b88a1`  
		Last Modified: Sat, 17 Aug 2024 01:59:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:21bb289fd3ab2237be0555958a46983b9ea817e10344522faa07c770d501de00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3198638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b53daf498e887c251befc7d43d87b6fbd226dc1ea1c312128efecf4d567cac`

```dockerfile
```

-	Layers:
	-	`sha256:9c569031e25d13c1c913393eda3be59341b14afb6475fe68f3205e7f6c3bdf96`  
		Last Modified: Sat, 17 Aug 2024 01:59:38 GMT  
		Size: 3.2 MB (3166252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e79c8a4b1d0f5c5af7f01c293a8d4183e8d6ac054b27ffe36159237cbb581e`  
		Last Modified: Sat, 17 Aug 2024 01:59:37 GMT  
		Size: 32.4 KB (32386 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.89-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:5ecb3205a373d8b3512d001e38b6d8f7eb5cbef572504cd5abfae4f03ebcf995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280777122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb302706c55291252d0d220b9d87ae22eaff8d096c5b2d7327f1987e73aa61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34fa575f3bac771ddb2aa598addd06eb8ee9021b249cbc0e60e5e9cd74885c`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 39.5 MB (39537820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ada097bad821da4edbdb4753ce1e3ca5ddf992a4bac4a2f723b4819ac2d96`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae55db9b5c5d4ef1702f1307c5604009843d2a03b7e3b4d1e671c0d3c95abf7`  
		Last Modified: Tue, 23 Jul 2024 21:29:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ed4eb688ce66b6712e8eb220e8a4f89814f673bb18755639d9b7b8046cca6`  
		Last Modified: Mon, 29 Jul 2024 15:02:04 GMT  
		Size: 852.8 KB (852771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aa3aa3c270f53227c94ac9f82f26be4cbe7ec5ec782011ef6e251ff3721633`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 1.1 MB (1053461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a9bb8833c4ee37b000b759ab55837ac009c53dee21316aadb348c7adde940`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9d88007be0ca432c6ceea4d60d14ce107db6cadd491c3092996f44407a9be`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 10.8 MB (10841725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f79c9540bac61a07eb070eab5cc2fdf86a86aa02529d84e1ced0ce6a0a473`  
		Last Modified: Sat, 17 Aug 2024 02:08:33 GMT  
		Size: 223.7 MB (223749457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff17ffdf21532d85f407d283c912715c58cc395bf8076465838a181393f1b2`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.89-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:45ed2a7d50fc18a0908a026e3c6d14db2ccdaecbdc94a7b5c6e57cb46e478c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a002c6c6b9caa196726a92f041cd11920ce4fae685212b86c9e5295ce002799`

```dockerfile
```

-	Layers:
	-	`sha256:feb498a45b5b54519fa9a472ad837b50abc9bdcad8ae1498547b49e38366638a`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 3.2 MB (3173633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19c5012399cea1277e97804afc4a9a85ca8791966ee7ff123976998df0d1e960`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 32.6 KB (32642 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.89.5`

```console
$ docker pull ghost@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `ghost:5.89.5-alpine`

```console
$ docker pull ghost@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `ghost:alpine`

```console
$ docker pull ghost@sha256:f9040f7b37636913dbcef816cef85223291f8805e1ce851dc0b3c001c6c84680
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
$ docker pull ghost@sha256:54dfa033303e4dbb83151d411d5f4629baeacecbe903dc40c7c539b833181be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261111640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d125830a91574e240dd7863a418c0951b1a501587335cb83ecdd4617857792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfd1a7f5d0b2ad6106b6097bf76f56d3a8c3bcc5cf7fa1f5d0a0ca9dc32cbc`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 39.8 MB (39831284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f16a148263d04e03d25d24411a9a48c71d7e31131900f4110b45b53c5a23ec`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.4 MB (1382231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30aa900b096c1999e57347eefc256ac6d0f228a2427efa4b8d9b2ec9152e74`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2858d9f271023c9c88bcd4e71bf3fe06371e91388edc3e3cc07bdb39011df35`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 776.0 KB (776022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d154c0ae41efc373dab0cc6e8f963ecd2997083bf297c49fdd87b6a529ce6ebe`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 1.1 MB (1121672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bfd53e00cac2e59a3ab7bbaccb72aebf710d112e2b0e513c4d2adcec7042e2`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97566d0aa7f0342ae696f178eff7c5a27b6fc691e8cc670d7199b58809ede67f`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 10.8 MB (10842758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77173a32cbd16d9f3ddb316667631dafd2077dd5dcacf359966955c4ab748aa1`  
		Last Modified: Sat, 17 Aug 2024 00:59:18 GMT  
		Size: 203.7 MB (203737436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce50ca1cfee8a0995eea27e0454f184d778b27d80536584f0c3483dd6872be`  
		Last Modified: Sat, 17 Aug 2024 00:59:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:60d341e0d921010c73032fa63d335cbe0333ea8182ff9538d39fe5ff4aca4054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c6154fbee2f94b3793ebfeeb61c8f8ee2d106890dce278b55eda473004a9d4`

```dockerfile
```

-	Layers:
	-	`sha256:c0d34ac0732e4e908bce7848d5066d1915d87ab4740fafc5a0b28f1c79b80a3b`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 3.2 MB (3173577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b23173063df968dbcfade140449c8feaa62b687db75e6c006a309b9272d323`  
		Last Modified: Sat, 17 Aug 2024 00:59:14 GMT  
		Size: 32.2 KB (32209 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:c2ac48262e1e735256e521b33ab4fe649858d671d0848c4d564f93697c3f4627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267849352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3e97dab5b29f53baec80515621bb3069feaa416f2e9d429fd5cd17c3a33489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31faeeb6568eb2da580663e85950ac0b00527da619bb2537ca4c06db51033c4b`  
		Last Modified: Tue, 23 Jul 2024 06:49:05 GMT  
		Size: 38.4 MB (38420236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3154e981db5c13ed905e8758cb01a65392f9a0fddec17cb0a5268c79c00a`  
		Last Modified: Tue, 23 Jul 2024 06:49:04 GMT  
		Size: 1.4 MB (1382242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d710ca75bd1b5c7448f0a5ae0ffe77eb30e3e18cbced8b2a3ac61359a20681`  
		Last Modified: Tue, 23 Jul 2024 06:49:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc97a7763d1ad9c4a6eb0eb073cabd71f82b6fbac5041c3fec7aad67ce7888`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 767.9 KB (767855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd0e71658dc455588dbf848c8aa8213278ed6d6762bb7d0a95d3a1e21b33f0`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 1.1 MB (1088933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaf43e4ac986fa2c0872fd605e5ec1b9a11a57160507b9d6311fd11ec709a6f`  
		Last Modified: Mon, 05 Aug 2024 19:16:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f8a66abc1a25f2f9c81a6a11661fd8419453dbce4a410d347fad6401a6545`  
		Last Modified: Mon, 05 Aug 2024 19:16:25 GMT  
		Size: 10.8 MB (10846335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25110d1a7b4a9a04ffec166ae497a3f95d9b9c88d87076481003f9ae6c953ba`  
		Last Modified: Sat, 17 Aug 2024 01:10:31 GMT  
		Size: 212.2 MB (212166888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792f689c4c7be57268305e55913fbd4d250863890ea99baa50746d5dc045bc88`  
		Last Modified: Sat, 17 Aug 2024 01:10:26 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:57abebea6fd33f63a400ec51d695505a58bb9a0421fbf6384a0e25758cf0f30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479b5d7d7d947b47bd50661f8607eaf67d35ae091311c0c824fb13657f2cf206`

```dockerfile
```

-	Layers:
	-	`sha256:13ef19686b52e27c843077e3cef297965e819c769e92e60540c730f4ec92cf59`  
		Last Modified: Sat, 17 Aug 2024 01:10:26 GMT  
		Size: 32.2 KB (32167 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1fd66d20684c5f7f7434e913a7c2b44f12166b2109b8245052b421c8d40ce414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266711115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5bafeec7942643428bd4ef8cf516675d2c840174e77e68d989a96da64a9ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f2aa85ba2de2b0a8671453c081dfb01400a67eb450d92f7bdde7805dab7d7f`  
		Last Modified: Tue, 23 Jul 2024 22:47:20 GMT  
		Size: 37.9 MB (37925178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380053b85efdf6375556fb6ed33dec58dab9f4b7864d30293edee2fe6e0f456b`  
		Last Modified: Tue, 23 Jul 2024 22:47:18 GMT  
		Size: 1.4 MB (1382243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a63c1dd0e066a189a6d24ee97b01453bad055bd325dcb882486d19eac11442`  
		Last Modified: Tue, 23 Jul 2024 22:47:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d3c66ca4e9316e52e59fadb69681c1aa7087bd2f9c197572dbdea20151ee78`  
		Last Modified: Wed, 24 Jul 2024 19:11:59 GMT  
		Size: 701.1 KB (701145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f09c6c5057a81da4bef6bfebde1bda2b8dfeb070a4198bcf115bbf03609d3`  
		Last Modified: Wed, 24 Jul 2024 19:11:59 GMT  
		Size: 1.1 MB (1088903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8668f5ac081c64a3e94ef25a7099299b8c991c1c8135c426ab21170d96c56`  
		Last Modified: Wed, 24 Jul 2024 19:11:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236031c27bb799c6f89ff2895432cce7b0e78e0dd83a2b5dffb1eb79180ff5dc`  
		Last Modified: Fri, 02 Aug 2024 00:36:15 GMT  
		Size: 10.8 MB (10841015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6a9571b854d42cdfbd8288ab7e88da5ec1df3650f7c11423f63c28015f78df`  
		Last Modified: Sat, 17 Aug 2024 01:59:43 GMT  
		Size: 211.8 MB (211844336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c339d9102799ebcfd86c78d66f65cc3207be2aedae173d18816988673f5b88a1`  
		Last Modified: Sat, 17 Aug 2024 01:59:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:21bb289fd3ab2237be0555958a46983b9ea817e10344522faa07c770d501de00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3198638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b53daf498e887c251befc7d43d87b6fbd226dc1ea1c312128efecf4d567cac`

```dockerfile
```

-	Layers:
	-	`sha256:9c569031e25d13c1c913393eda3be59341b14afb6475fe68f3205e7f6c3bdf96`  
		Last Modified: Sat, 17 Aug 2024 01:59:38 GMT  
		Size: 3.2 MB (3166252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e79c8a4b1d0f5c5af7f01c293a8d4183e8d6ac054b27ffe36159237cbb581e`  
		Last Modified: Sat, 17 Aug 2024 01:59:37 GMT  
		Size: 32.4 KB (32386 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:5ecb3205a373d8b3512d001e38b6d8f7eb5cbef572504cd5abfae4f03ebcf995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280777122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb302706c55291252d0d220b9d87ae22eaff8d096c5b2d7327f1987e73aa61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34fa575f3bac771ddb2aa598addd06eb8ee9021b249cbc0e60e5e9cd74885c`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 39.5 MB (39537820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ada097bad821da4edbdb4753ce1e3ca5ddf992a4bac4a2f723b4819ac2d96`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae55db9b5c5d4ef1702f1307c5604009843d2a03b7e3b4d1e671c0d3c95abf7`  
		Last Modified: Tue, 23 Jul 2024 21:29:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ed4eb688ce66b6712e8eb220e8a4f89814f673bb18755639d9b7b8046cca6`  
		Last Modified: Mon, 29 Jul 2024 15:02:04 GMT  
		Size: 852.8 KB (852771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aa3aa3c270f53227c94ac9f82f26be4cbe7ec5ec782011ef6e251ff3721633`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 1.1 MB (1053461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a9bb8833c4ee37b000b759ab55837ac009c53dee21316aadb348c7adde940`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9d88007be0ca432c6ceea4d60d14ce107db6cadd491c3092996f44407a9be`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 10.8 MB (10841725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f79c9540bac61a07eb070eab5cc2fdf86a86aa02529d84e1ced0ce6a0a473`  
		Last Modified: Sat, 17 Aug 2024 02:08:33 GMT  
		Size: 223.7 MB (223749457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff17ffdf21532d85f407d283c912715c58cc395bf8076465838a181393f1b2`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:45ed2a7d50fc18a0908a026e3c6d14db2ccdaecbdc94a7b5c6e57cb46e478c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a002c6c6b9caa196726a92f041cd11920ce4fae685212b86c9e5295ce002799`

```dockerfile
```

-	Layers:
	-	`sha256:feb498a45b5b54519fa9a472ad837b50abc9bdcad8ae1498547b49e38366638a`  
		Last Modified: Sat, 17 Aug 2024 02:08:29 GMT  
		Size: 3.2 MB (3173633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19c5012399cea1277e97804afc4a9a85ca8791966ee7ff123976998df0d1e960`  
		Last Modified: Sat, 17 Aug 2024 02:08:28 GMT  
		Size: 32.6 KB (32642 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:27b2029266d5ef5f36d13e201a58cabfe75f611ca74afa0e7f693a06fa8fa692
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
$ docker pull ghost@sha256:86786e9fd3a318b1e3e047cdc6e0c86f3b89a5048a916ac5e37937811e55e9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287856892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab6d0ae7ae1809d944207c72426c01285be8a3d5d6300d30f91c571da7682fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a229b4e56f545f0831dcbf11ad1a896cda878b6fbc45114e57fcdaeaffcdc3`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42c00a0ef3813e6a0ceb58e667d811154a603255d660c9d837195a348d0b80b`  
		Last Modified: Tue, 13 Aug 2024 01:12:45 GMT  
		Size: 38.2 MB (38179073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f862ff7d95856d2b0773115c655e0b84e04dd46f83103cd3f264f8ec61e4e1a3`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 1.7 MB (1708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1326ef1e29286982806dcc11f5f4d5e8289c26030f2556d11e9c193ab45664c8`  
		Last Modified: Tue, 13 Aug 2024 01:12:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ab289f7c2e68e2272b9a20dc7b47fce8cc4e017401fb8295cf21f1299265c`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 1.4 MB (1444700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3888defbab8e0ac28287ba3a82bbce7e1983bb9aa83e8e577b7708ee4bed511`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 10.8 MB (10842078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17351c9f41d78f46470f11f774df133f8bab7198107969ef0ec2e7532195c8b2`  
		Last Modified: Sat, 17 Aug 2024 00:59:35 GMT  
		Size: 206.6 MB (206552454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b31fb887501b4dd17c40a75b2745d5d763cbf49250c1c2d87fe79a8f3f820e`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7bb1f04f1250872649ac20f746c1caa2eac731baa6477ccd733518cee77f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b3110322466a372c955e2f12c6e28776bc809b369e16741d2c42b2f3a4faba`

```dockerfile
```

-	Layers:
	-	`sha256:55a8988909e625599a296e895e1216fdb782e55d25a19fb3985139492c37c68a`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 5.3 MB (5271310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee52f856bbbfdd89570c0f0d81ca935d05f7d0c3fedf43883fddad2a0327deee`  
		Last Modified: Sat, 17 Aug 2024 00:59:30 GMT  
		Size: 29.3 KB (29267 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8d9ca7d47cbebfc2f39af16450f7e77ac6704627b7e12e49ba3a42bb9c868244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300406464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae0d38525a13ee5dd6d7680c2dad4ed529e44ff8f780f3a537d40adda1b7077`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca72af6520ab6cccdc25464c65a8886151f7eb3d3a68e4343ffdf07091bd15ce`  
		Last Modified: Tue, 13 Aug 2024 12:11:23 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90c93a4630f341b7911be4328e41219dc2e76bad885dcd9d182fe5aa1f1429`  
		Last Modified: Tue, 13 Aug 2024 12:22:38 GMT  
		Size: 34.8 MB (34834276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66955684eb5d036fd9e9b8474e766ec45fae24ce6fb3bff5487954a54ef50b85`  
		Last Modified: Tue, 13 Aug 2024 12:22:37 GMT  
		Size: 1.7 MB (1708463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ae18a246047f8d8ecd4bb4233dd7c39ed15da3b8bbea336431487f4acca51b`  
		Last Modified: Tue, 13 Aug 2024 12:22:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee59bc43dd129fb9bde542e4dada2b6259f095881d22a027c93fdc9fa40c00f`  
		Last Modified: Wed, 14 Aug 2024 03:00:20 GMT  
		Size: 1.4 MB (1412523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd9aaf39418c7f326bf1239ea91620f12752037ed7e554e3a59da45f119be1e`  
		Last Modified: Wed, 14 Aug 2024 03:00:21 GMT  
		Size: 10.8 MB (10840413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a560f52061cc80aeaaf5b7f84af8b106b83635c37c41ae0e2bc8ff313348f4e4`  
		Last Modified: Sat, 17 Aug 2024 01:48:50 GMT  
		Size: 226.9 MB (226888319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529c220b1a13ab629f9cf5dd611931720a14bedd2706e7268cbd9390937d559`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:20bbe2301d85efc17cba1d50f0a64d3999847375aef6e0a1475fd9eb144b4d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6afe9b6590324bf389faf2defed6e81d0f46214583ba877d2251c80df79e8a0`

```dockerfile
```

-	Layers:
	-	`sha256:b7f8bfc89f44af440cc1fec387e31397a22c7d14b1be282dd5aa293b910ab743`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 5.3 MB (5276673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5453e31a8a23b9dfa3a466c1fef976c6b287c3d12d73b0b1f36a0e8750707c71`  
		Last Modified: Sat, 17 Aug 2024 01:48:45 GMT  
		Size: 29.4 KB (29405 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f2b4f0aab8ade41346601936a2f79349c122b42ef67c9c5a6e27b486ffab2f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288823816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e00ebac3611e8a35e03dc526f13c2ad2d0a5b0a7818b88f47d2cf8416a36b9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f5aecbd9ca490d421ea755047a15006ca127eb80f50d917b9b7ea9a00327f`  
		Last Modified: Tue, 13 Aug 2024 07:45:15 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1472ebe15cf68957d51ffd887cab0b99d25048f78fa7c327f016cfa940e9b0b`  
		Last Modified: Tue, 13 Aug 2024 07:49:19 GMT  
		Size: 38.2 MB (38223538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c47224750647d76572fb2d716ce23438d387b48354c1c1e02c684d67b6a77cb`  
		Last Modified: Tue, 13 Aug 2024 07:49:19 GMT  
		Size: 1.7 MB (1708240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9535a7db32f846d51a8e37c90c4d2f11bbe9c89a128d060aa7fbc210bdbd5d38`  
		Last Modified: Tue, 13 Aug 2024 07:49:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ab6a798ab76d3e208b95993058b9ef3d31dcdaa47c3c58606382342407279`  
		Last Modified: Tue, 13 Aug 2024 20:18:42 GMT  
		Size: 1.4 MB (1376502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6e7f548cfc5e04a68b39799eb888da995ea3d3ec6a38279ccb26a769fc7c37`  
		Last Modified: Tue, 13 Aug 2024 20:18:42 GMT  
		Size: 10.8 MB (10841798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3659d795ce52c30687b8a407b818d44caa13d8b8b031aa952b292a5a43f277dd`  
		Last Modified: Sat, 17 Aug 2024 01:56:24 GMT  
		Size: 207.5 MB (207512879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3405fa6bdb88b697f2eadb93bbc91ce0f1a41e8341529a3075754d703b5d6a8`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:24dd03632d1011a33ec32229a0fcc467b08e5192942ae681dcf4fd1ec03084aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679c70dc47f230134e6941a25bfa766b0eed89b463a9481b1ff2ab9a8fb6001`

```dockerfile
```

-	Layers:
	-	`sha256:525dc5bc5e77f770153d52d1a6002dfe8d0a535cadb04ab86ad07849ce48732f`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 5.3 MB (5271560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f7a753fb10f94c4ad8307eacd1fd1cf32b4ab56be113ac1a9839e27c2c2fd3`  
		Last Modified: Sat, 17 Aug 2024 01:56:19 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:330f51f67333f7e144e27d22c378ff4d69ddbe9853836d46dadae44b38440520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301390889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b364fc36d159226c4a9e8872bc0512514289485114bd796e3ff5f1b4f1da93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5d8671d229877e86fab6fbbd80fd27eb274b2e69afefcdfd5ce4275304f103`  
		Last Modified: Tue, 13 Aug 2024 07:18:23 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c61ee5c081a173a619d65a0dd7744322fb2b4f174d5982d841d6e8e548c65a`  
		Last Modified: Tue, 13 Aug 2024 07:25:28 GMT  
		Size: 40.3 MB (40263153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b58dcbd8199492954fcf3b474b6a13a98f571d8ff1daafb001a22802d65f948`  
		Last Modified: Tue, 13 Aug 2024 07:25:23 GMT  
		Size: 1.7 MB (1708394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10b147a72719064981da776661a474b2fc3198427bc803662c7e67ed4d8d65e`  
		Last Modified: Tue, 13 Aug 2024 07:25:22 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574890800ac29a91e7db6120f8b2fd2cd1d50aa450e726ef69a0d71ff61db677`  
		Last Modified: Tue, 13 Aug 2024 22:39:31 GMT  
		Size: 1.4 MB (1366626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf9db1cac32d5705261307f7420e0e0e51837c368172bc69b43ee2ba024b5b0`  
		Last Modified: Tue, 13 Aug 2024 22:39:31 GMT  
		Size: 10.8 MB (10840074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9249d5d8a8decf1600cc9eff1abd23d76bc59adb762b4a6b42bb4281c8ae70`  
		Last Modified: Sat, 17 Aug 2024 03:55:53 GMT  
		Size: 214.1 MB (214086010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eb9a4284c7a1945456a7a30881f0cbbf74709696a9032e47ecec92e236ed46`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:67e3ce798f6e71cce1a6b6070523ae64a7cf9daf9396d7355bda43318c68c090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413b85452caae755fd4da6803d89334e69a3a3f85cf2782d9eb8765f776159de`

```dockerfile
```

-	Layers:
	-	`sha256:491069186e918e9dee07687c1d878e80887c143430b6a8687e792fc3a88d4506`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 5.3 MB (5268206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de62f7295637aacd421f58f7cccaa25106939a85af615df0eaba82fe35ad4fc7`  
		Last Modified: Sat, 17 Aug 2024 03:55:48 GMT  
		Size: 29.4 KB (29351 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:ef7bf2caa8d2bafaac50412ab160b55c7c3e8cf39c3dea8ae8a90e6225967d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293929008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebe13ade283f37cf0057faa641308a5fe6e7537e5c77c48274c2114d89c16fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Aug 2024 20:19:14 GMT
ENV GHOST_VERSION=5.89.3
# Fri, 16 Aug 2024 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Aug 2024 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Aug 2024 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 16 Aug 2024 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Aug 2024 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e5af7951f31ebaf8f18c4c3376d0d0bfdfd054ba6458d447fa7553077201d9`  
		Last Modified: Tue, 13 Aug 2024 05:41:02 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8085eb5c05d7c778cf29d785e9c38a9745b75f27046ccfe042db2bb8867cea4`  
		Last Modified: Tue, 13 Aug 2024 05:45:46 GMT  
		Size: 38.4 MB (38403871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1770d19b5d24606d5de2201575fcbf046e4f4b9fdd1bcfcde321bffde569fd`  
		Last Modified: Tue, 13 Aug 2024 05:45:45 GMT  
		Size: 1.7 MB (1708142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5376f828cedb7c818dfa096f2b13c0798666f7343cda359f0e775321ef59b2`  
		Last Modified: Tue, 13 Aug 2024 05:45:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb1204457289986dce2001365927b5dc939a5d8f15a43bb5f2c51a6c60f06f5`  
		Last Modified: Tue, 13 Aug 2024 21:45:58 GMT  
		Size: 1.4 MB (1410231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bf7ad47adf940e4597085675e78fcc6d423a3cbbcab8d91bcbff90fed70309`  
		Last Modified: Tue, 13 Aug 2024 21:45:58 GMT  
		Size: 10.8 MB (10844553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfca19625014dca23d4d300f9ef42f52d3bd29dfd3547596749c1127e163e52f`  
		Last Modified: Sat, 17 Aug 2024 01:08:13 GMT  
		Size: 214.1 MB (214067783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8160d53e7bfbdacb3e2f43e2cba14d82cf553b61376087ae61eb27bac17311`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:1d62252aff02d86a08ade55028b346859b8e0cde452e593b04ec3d6de2cb82a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9367dfbdc308d1a4ce9df061c32776d1e75fc2587092d8286f3c821e5cf63d`

```dockerfile
```

-	Layers:
	-	`sha256:752919c41d6d947fcaa762b7c3c5112a03c49c8063f90ac81af429d78ab587de`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 5.3 MB (5263786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82fdae27c16cf8a0b94d324d66715195ce2279cb821e31f651ebe4309de4212`  
		Last Modified: Sat, 17 Aug 2024 01:08:10 GMT  
		Size: 29.3 KB (29303 bytes)  
		MIME: application/vnd.in-toto+json

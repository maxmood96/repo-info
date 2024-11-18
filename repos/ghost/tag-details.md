<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.101`](#ghost5101)
-	[`ghost:5.101-alpine`](#ghost5101-alpine)
-	[`ghost:5.101.1`](#ghost51011)
-	[`ghost:5.101.1-alpine`](#ghost51011-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:93ff4c2dda1531782a52175fd42cdd3a278c318d6b8c897af737eb06acfd62b1
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
$ docker pull ghost@sha256:6adda1218d7db5552dff86974609220c47c5b42455877758bf771833acbe90a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174858883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e767e7d7923b8919bcf7a828a89c0363dbf0511857c5954add8c4029cee2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1a8e62161bc0632b3015ed29f3acd39ad51967b9f520b7fbca4b87d4abbfc`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a420fb4222f0ca00745cba1f93c448edc40483577dd3293abc23411009bb5c`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 38.2 MB (38233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e947ca9116f18eee431341298f0ae84403e13b359264a10d8358cf4766fbb0`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 1.7 MB (1712393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651c84feb4c5f72324ad867e61b43fbe28a681bd83493219a6dba60cf1dbf6`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15990d70afcacd012de19dc75538eafb360d11efdfe9676262b2a856755c31f`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 1.4 MB (1444746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be436f9b3739a5ed1c8a35370b8428efdabafb812bca44a69d8e98a2b518dc52`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 10.9 MB (10886453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d542188c5707d31aeb0f29119b5baa3b7c4dd84695779828ffc1571c2054e`  
		Last Modified: Mon, 18 Nov 2024 15:49:33 GMT  
		Size: 93.4 MB (93449346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29ef52eff3cfe8671ca39667c8b9f1a3b5c24acfcf4e4f98c081fbafdf495a`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:668435a744e259d426d0e29c09881d1c2060ebb677e4312277bd2c20c07cf3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a631f2c2445e543838043b99b674ca785c498c5678645c03dd54681b335b29f3`

```dockerfile
```

-	Layers:
	-	`sha256:faecc37e3bfb421e312d7e910108ef0ca5b430f410ea358ff7b580c156e04681`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 5.4 MB (5431222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6686300074dd68d5356dc3d9811ffb58ae4161d8c18e14d37801c2cb2ee078`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fdba2da346f989ded93d0381a78b52b953826757e88cd44f073ba2c2b6aa7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187348764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa26e0ac62ed60d585437970be8cd16770d9dd3a837e0310558dcf98f3b84e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12e8f4279bfa57e91b124afb54540f003f2bca339945f6a92e0fe2521df05e`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c10b5c43ca02ec06641a0ecab5bbe328afe13154fd9b2d5b07c2b1e5dd31c4`  
		Last Modified: Tue, 12 Nov 2024 23:46:57 GMT  
		Size: 34.8 MB (34834213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb1880d4b7c1d0c9cc7a18adbafb6d5c0dc15fe9ecc0963d0acebbdd5dd54a`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 1.7 MB (1708399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f51d33dfbc7d2eff0b37c55149300e299820a5b3dc556b8879f773c0f928741`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121220baf3c300e0dd3aa98a69e6532d9d7bc0595f7457cba1fe3f0d60e0f9c`  
		Last Modified: Wed, 13 Nov 2024 14:36:25 GMT  
		Size: 1.4 MB (1412399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a2999a7a218d7e7db282d9394133403e8d637d1b8771767918f5ce6615913`  
		Last Modified: Wed, 13 Nov 2024 14:36:26 GMT  
		Size: 10.9 MB (10871790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507e56710947c4dd3083f67fa34456eebb4c6bdbc143ba341e3fa55b672d5fd`  
		Last Modified: Fri, 15 Nov 2024 23:16:10 GMT  
		Size: 113.8 MB (113798721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2590da70ea99acbc45c33af0e63690eb64eda91a739b149685146e26ac689ce1`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:51a79a847028b42640232a4f0cb52fcf6d3f8286a7712d64851558161d92ecfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465b25b619a2a59b8f9f8717ecd23e5ede5152d85c880b749e6729516c043878`

```dockerfile
```

-	Layers:
	-	`sha256:041a408bdcfb53782faf4553286f62b37627a0eda1c6dba47432c696f450baac`  
		Last Modified: Fri, 15 Nov 2024 23:16:07 GMT  
		Size: 5.4 MB (5442051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3210eb1fa6df8628b4aeb6e0f361960031cd81866b9c0cc1cffde16951feaae2`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b5de05b12149bc0e70c6d198a1355329773d651e789685c7312e3893ed9f84e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175855658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542706cc8f6ef6147c674b68fbc870bf5398117d8c1aacf6ef7efc7135fe9341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd83c78bbcfdd59177d67cdf89d1ccebb974e65ce433046486c1e297458a71`  
		Last Modified: Mon, 18 Nov 2024 16:57:30 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f209b7eb95422a153127b9a38a0d045d24287397e8b9d9ae3200442bf75d274`  
		Last Modified: Mon, 18 Nov 2024 17:44:45 GMT  
		Size: 38.3 MB (38304628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33194ef90e970e5976ac687ef339159661c5eb2e65c8d475bce213c9203dec7f`  
		Last Modified: Mon, 18 Nov 2024 17:44:44 GMT  
		Size: 1.7 MB (1712458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd4d3676c518b3a1b588c15c6b3ce261adb6d213780a32d8f17d15ad402edc`  
		Last Modified: Mon, 18 Nov 2024 17:44:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa547ff5f4f418b328c42bf29a767b530aaf653cc22e28dd01bf076a574d6a`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 1.4 MB (1376512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40471a53cff3131aa22de8b8b09c60f08cfce29c6da815937a5f21551cafd64`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 10.9 MB (10886537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4925238f229c0ab8be0f43f06953c20cff33a3f7d651c1dfb96b1762ed18a4`  
		Last Modified: Mon, 18 Nov 2024 17:49:43 GMT  
		Size: 94.4 MB (94413827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ecaa1d170551cc46d629ca7442cc310db1f24a4f2fa6cb5cb1e2eb8e594ff0`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:21dd101fc39119378c1617a26e3adf62b6c436548c9e92ded338f99d6e59b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d0ca1207a5253ad06d841fb27cc82d1734673cf09c1299872ccd59e7288ffe`

```dockerfile
```

-	Layers:
	-	`sha256:2f04b8e6d88b44b2409a14eee8b3d5a81d47e27699755107c93ecae166e7563b`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 5.4 MB (5431472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92259aae7eb20f16ca913b4a047a10ea4ccffb609db397f834a6bb8e1213aaa2`  
		Last Modified: Mon, 18 Nov 2024 17:49:39 GMT  
		Size: 29.4 KB (29440 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:a42d82e08f68045aac512d8a90b3cb43717affe18810b776ee5a218338dbddb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188438582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217979c19dc7b34eba5e3abde0ff4bb5b5a5db88a038315cf4341d773b0e55c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b818420b8b420d93637d67bd46b71029bfb1e062b744b14c8f79e7a7cb6589`  
		Last Modified: Tue, 12 Nov 2024 09:03:45 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d859570a00ca2b65000799fc1cdd091706ff08e28882bd44d6d6d3152e20c`  
		Last Modified: Mon, 18 Nov 2024 15:41:14 GMT  
		Size: 40.4 MB (40351609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8924ec273e919caf7a8a1210fc8992a235b183678e7686dd941b3f295287a`  
		Last Modified: Mon, 18 Nov 2024 15:41:13 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b1adc6ea76ee1a63da85d99c948134d2f3a81ea73d7383aa5e8c3878cc1e5`  
		Last Modified: Mon, 18 Nov 2024 15:41:12 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d34ba125482343643488b81300b7f2ce0aed0c6695145a848c73f0925e5e2`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 1.4 MB (1366618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86e8cffb2db3795823e0a1b7a686bd540c5d02918ef232ca6173d60e2c82c1f`  
		Last Modified: Mon, 18 Nov 2024 15:57:45 GMT  
		Size: 10.9 MB (10890010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff12d6c364e7c870226185011eda5f11ab082357b9d1e1f1fc7083807a1491`  
		Last Modified: Mon, 18 Nov 2024 15:57:49 GMT  
		Size: 101.0 MB (100987987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0da1180f914637f06b82c1be6eaeda13df6c62142bd6bc7c25026bbb9c921f0`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:9e5841ed29ecc752e24909d28f52d776a7cb08c5ea10a5ecdafbf943f4e085cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7b4e806e2e543eb2b07196bd3deca075e913024cb28376da6205288ce17b96`

```dockerfile
```

-	Layers:
	-	`sha256:a930f663b0655f899dc638f1eda5b9af40fda08089b78bc0e5697cf4b1a77277`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 5.4 MB (5427476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce245dd38ad15f6264d37c3569780606360fb353c9f27db162b6229a8c224c0b`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 29.4 KB (29358 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:a326c789845b43e67fd70ea192992d31dcf818df5fd6767ef7dda74b8223dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180850920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7be82c62dbd13412005728f285f630b21a101f86d5e0c8e37222f0422d35a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5936a9967200e38b9edc3158d32d0bd35fcdadb6ce24041a0fd1a4c31f82bac`  
		Last Modified: Tue, 12 Nov 2024 12:15:56 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34127b12d15850d7834b1077b8c55b769151447e9c26ef585c832e35d5caa0f4`  
		Last Modified: Tue, 12 Nov 2024 17:32:29 GMT  
		Size: 38.4 MB (38403967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682b50f1b1c57d9a4cc8e4b2569ee33bf7d2c5afd57964c5efc69d5bb09df5bb`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 1.7 MB (1708311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068d72d677c3a3b185ce6bb3b5db7e1eb7b1ebd26d8ab52bcff4d7ed2bf6693`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e40c0afde1ff131a4380bd2bb16012712b2bb9b091b56f14888438f693baecc`  
		Last Modified: Wed, 13 Nov 2024 02:22:49 GMT  
		Size: 1.4 MB (1410261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f92cb1aeadc76a8e91374dca4bf3f04465601adbea07f9aa36d57660d4895`  
		Last Modified: Wed, 13 Nov 2024 02:22:50 GMT  
		Size: 10.9 MB (10869645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e6a2863f96037bb86576689a3dd515773e4b3d43e3e4e33ada9ea731e079b2`  
		Last Modified: Sat, 16 Nov 2024 00:10:10 GMT  
		Size: 101.0 MB (100962775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce9224d49b17f4577f5291a40b93f3b124466f532d43090377266a1de80ca62`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:cbd04823c522f5a854665ce8382f3324c65be685bc14e2b857e44a699be89ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131f693be06516c73c7409d0b3f78cf906d14b077cfed59b642f240f8965d7dc`

```dockerfile
```

-	Layers:
	-	`sha256:e4c0e1beb4eddfc2be9cbc018f270692a545b3f1dacd08ad645ed806cacc7699`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 5.4 MB (5428310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcc27429a3bcb37b1d410f808d89f1e0f11e5f4c2ee74903451f87ec39a059a`  
		Last Modified: Sat, 16 Nov 2024 00:10:06 GMT  
		Size: 29.3 KB (29310 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:18374c65f40ddadd1891e8d7a5ad2c5194248d1cb4c18772a367b7fd2e8ca536
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
$ docker pull ghost@sha256:1f1f74109cbbd5ee6c39119f01c3f02c4d9273d45045dab12b95b879d522429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148314439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87f98b1fd1ac9710b0d618841c05141ac97c528da4a1b6963891198c256df26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5ba5322b4a5416240b08583db88aae9b9138dd36fd54aa9d20173c3db57851`  
		Last Modified: Mon, 18 Nov 2024 15:04:48 GMT  
		Size: 40.1 MB (40091144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c4a69072cc1e5ba000ae076927371dc1d755805dfc729ae27814d9b8ada2f`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36d32de04200f805172fdaa1bbe7a28053ec150a9b4cc181803fa3f44d8be09`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304a60e90041b1cc9cd91553b7d697e15550e292740c3c76794b9621805f775`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 776.0 KB (776023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dee8aec1a555510b06e12d3cd69c471ab3fe1cb9f7b7db63bb11ce05dcebce`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 1.1 MB (1121665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9475f3353914e8da3bea48022acf27cc5603b7e79b3b73a7bf897ab53c28acd`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca8aae3943880c5677429fe4aec791aa311a7d03a63469ffb68278f13a1288`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 10.9 MB (10885270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c6f70ce981c85a6364b736b6fc34a760ddc039646a5e7c88603b780e0be394`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 90.6 MB (90632188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9bc7a5daee07471c168be1fe888dabab39cf0ae559f10f16bd5ed9497c23e`  
		Last Modified: Mon, 18 Nov 2024 15:49:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:505c3b5912be58a3e1f08b24623deca7afa7464dbe75ff5c939138602671cbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dfc73487013b4de2d77c00840acbd4aba06541c4e6cff3adc101148902cf58`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa258f4ef14668447ba76bf7472321c92ee4b6cd005cd3d507a65a672d714a`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 3.3 MB (3322041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3805ec0ea0654b419ccb3f4ede0e8a2cb4373f41b4abf86476af5de88e7635`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 32.2 KB (32246 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:238949b177213fd865adc8667c565246c683e32a1b3d09f387193826050237d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154792064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a61a3d99ddf4c68cb84b5f0ffcd8609b88b2bc32178adba3e8724ace7bc7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5303b3afb218972eabf2203cb43b270ec96e28d49e0910900b0454f7cd15ad`  
		Last Modified: Tue, 12 Nov 2024 13:13:47 GMT  
		Size: 38.4 MB (38420266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac520e29cdd00b18e0a99c1da3851dc793f477a23eb22c051090e229318e9d9e`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 1.4 MB (1382250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e1218025d1d9d0b50ce6a18083d3642e07564c09f946fe7ccac4af14d1cd72`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12878dac288d46e798fc65b46ffc0069f31dd9d62fe3c28c3036e81fdf370daa`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 767.8 KB (767849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb19f8ebb4e341a0b72450e667b8518b41c8d12e44b365b7845cf7473064463a`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 1.1 MB (1088936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327b34e6e3bc78353d642c4f368171cb7245701de1a3df520dbbcd6dbdf68930`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a8ac45478fbffdd11d363cc812684b0f9a47263252425c064dda1291690388`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 10.9 MB (10887483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf4470a8e65453783ef724279c83670f49eb5d0f804f9ea9a69bf65fc673c9`  
		Last Modified: Fri, 15 Nov 2024 23:19:10 GMT  
		Size: 99.1 MB (99067660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d71695876930af3fedcc44df4cc38ceae365216e344959f6848d0542eafbfc`  
		Last Modified: Fri, 15 Nov 2024 23:19:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2b4e8c448f26e1243d430fa2396d99982df1995e9a03707161580b8871710242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6074401562c738383fdea6871eeb2debe8a1ff0e186b2f109c3b42ba0f15a`

```dockerfile
```

-	Layers:
	-	`sha256:548cda8cd16e4cfd1f9fa406331ffc0ed4233b7e3f35f8acf1128852a3ef4333`  
		Last Modified: Fri, 15 Nov 2024 23:19:06 GMT  
		Size: 32.2 KB (32158 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b08439262a81da78fabb8c34d8a635c9c78c301c18b5e9d41ded7c4014096afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153652792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ffff1aebc7d8da4d09f032cf3fc23665fa6d25cf09f71ac53329ab27ef997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace86978619da2f36047b5cbdbd518e2f3981dd44cf545695c7e7d04170442d1`  
		Last Modified: Tue, 12 Nov 2024 23:21:38 GMT  
		Size: 37.9 MB (37925094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8250d0c0ebf3e9e5be6339bacf03360dc4fa1b5b0fe6a7c9aa916d91d959e`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 1.4 MB (1382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46313ae619e2b3cd9b20ce8d6ccf91e56398fc35c81a19b69d3253a68af4f7da`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fb97108fad0c6fff92bf6e507d46e7dc4fb65661e50bc0733747b6ad1a667`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 701.2 KB (701151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ddaedc2788cd21ed9d5e9fcfc09d0f7145966762d8e39a293dd79e08bb5678`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 1.1 MB (1088905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1473a48abffd7c0eeb6a49dd88b9bf462c7cbb152fd068c095b6a8698da30`  
		Last Modified: Wed, 13 Nov 2024 14:46:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f89d31231794101e907fc69b00faec60df311f773eaecec1a05b91a35bbdce`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 10.9 MB (10871426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7a993d59db0b8ed2785fb42f58f35171c3228b1bcb1a48127127aa82114169`  
		Last Modified: Fri, 15 Nov 2024 23:25:57 GMT  
		Size: 98.8 MB (98755042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248b6c06ec8bcc232e75f32d5b24d4b19c2c9afb5723b75bf30627887dfc3ae`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:297f563b7714786a047939e69d35cbb6626ff07fbf88ff64526bac71c8651ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb1a4d37cfe9cafb4de39ca3a20eeb8f3fafe7c2f54491086767403a508e109`

```dockerfile
```

-	Layers:
	-	`sha256:506ac704993e74231440f52fbe50e21974d6e78e56df1d20659110aaaeab187d`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 3.3 MB (3319434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b34d600e500f16220aaf2c7753747f3c78d677c83e3d3d9342f71ec7292bd`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 32.4 KB (32374 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:bd40723939738d573d37193256e92964575db0e07b966dfd1688f13d9f1957b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167814019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81b595fbfba87ae253192ed5f2ee9410f325db1370a7e75483261775b99d8da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145d210cb54045f3c727468bf465a3f263ff707a64da19e7d5d7f39680534637`  
		Last Modified: Mon, 18 Nov 2024 17:21:20 GMT  
		Size: 39.6 MB (39614415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc6f17d6ed2208b0d690e9e6ca3e3704177f4bbf02182a206951021f7b401c`  
		Last Modified: Mon, 18 Nov 2024 17:21:19 GMT  
		Size: 1.4 MB (1387220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628a8cd3385e1d2063448f845b9b3f70a2834e0ceb45f5e0a035e2a39d5e51bc`  
		Last Modified: Mon, 18 Nov 2024 17:21:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fba904282f0ae4661eb40bb1a336279a8c7e9af817034c5145a8deca9cb58f`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 852.8 KB (852762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd011e73ee54d748bee7de6a4a9974a246cd5f72ca059ee99d4405759745cd40`  
		Last Modified: Mon, 18 Nov 2024 17:53:34 GMT  
		Size: 1.1 MB (1053459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d41d78063ef9e70d23b6438b16eed5d96517c0b78d730e6cffac2906ce4ac`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8b461b47a202bfbff2e5bedeb7e7bcd04c07a03a67abc603096088efb14d1`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 10.9 MB (10886849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26d62a97f1c90f865c67eab88a3a756ca08e055df223e6bcc8024d5d7cfe4d`  
		Last Modified: Mon, 18 Nov 2024 17:53:37 GMT  
		Size: 110.7 MB (110658882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fec79d6636ddbbcf6e0e192d19455a1634867415f35b3198b09c8aa685556`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ccbd6f0e337395587e428bd68e0974485847d3962c52a31fcac0bd807edb6aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc5a3ba93c431b889aad9e2b05d9e865d3b6fbc4173909b3517105f8b58268d`

```dockerfile
```

-	Layers:
	-	`sha256:84ffb304164ac8a02b781b4d307175e2ec11a8f58cd3f1efc8b962ece4b7daee`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 3.3 MB (3322097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330334c78d29fe9ee2f7771ed9599d6db5efe037b9e9ddf7f965f05365f5322e`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 32.4 KB (32411 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.101`

```console
$ docker pull ghost@sha256:93ff4c2dda1531782a52175fd42cdd3a278c318d6b8c897af737eb06acfd62b1
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

### `ghost:5.101` - linux; amd64

```console
$ docker pull ghost@sha256:6adda1218d7db5552dff86974609220c47c5b42455877758bf771833acbe90a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174858883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e767e7d7923b8919bcf7a828a89c0363dbf0511857c5954add8c4029cee2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1a8e62161bc0632b3015ed29f3acd39ad51967b9f520b7fbca4b87d4abbfc`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a420fb4222f0ca00745cba1f93c448edc40483577dd3293abc23411009bb5c`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 38.2 MB (38233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e947ca9116f18eee431341298f0ae84403e13b359264a10d8358cf4766fbb0`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 1.7 MB (1712393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651c84feb4c5f72324ad867e61b43fbe28a681bd83493219a6dba60cf1dbf6`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15990d70afcacd012de19dc75538eafb360d11efdfe9676262b2a856755c31f`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 1.4 MB (1444746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be436f9b3739a5ed1c8a35370b8428efdabafb812bca44a69d8e98a2b518dc52`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 10.9 MB (10886453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d542188c5707d31aeb0f29119b5baa3b7c4dd84695779828ffc1571c2054e`  
		Last Modified: Mon, 18 Nov 2024 15:49:33 GMT  
		Size: 93.4 MB (93449346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29ef52eff3cfe8671ca39667c8b9f1a3b5c24acfcf4e4f98c081fbafdf495a`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101` - unknown; unknown

```console
$ docker pull ghost@sha256:668435a744e259d426d0e29c09881d1c2060ebb677e4312277bd2c20c07cf3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a631f2c2445e543838043b99b674ca785c498c5678645c03dd54681b335b29f3`

```dockerfile
```

-	Layers:
	-	`sha256:faecc37e3bfb421e312d7e910108ef0ca5b430f410ea358ff7b580c156e04681`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 5.4 MB (5431222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6686300074dd68d5356dc3d9811ffb58ae4161d8c18e14d37801c2cb2ee078`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fdba2da346f989ded93d0381a78b52b953826757e88cd44f073ba2c2b6aa7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187348764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa26e0ac62ed60d585437970be8cd16770d9dd3a837e0310558dcf98f3b84e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12e8f4279bfa57e91b124afb54540f003f2bca339945f6a92e0fe2521df05e`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c10b5c43ca02ec06641a0ecab5bbe328afe13154fd9b2d5b07c2b1e5dd31c4`  
		Last Modified: Tue, 12 Nov 2024 23:46:57 GMT  
		Size: 34.8 MB (34834213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb1880d4b7c1d0c9cc7a18adbafb6d5c0dc15fe9ecc0963d0acebbdd5dd54a`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 1.7 MB (1708399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f51d33dfbc7d2eff0b37c55149300e299820a5b3dc556b8879f773c0f928741`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121220baf3c300e0dd3aa98a69e6532d9d7bc0595f7457cba1fe3f0d60e0f9c`  
		Last Modified: Wed, 13 Nov 2024 14:36:25 GMT  
		Size: 1.4 MB (1412399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a2999a7a218d7e7db282d9394133403e8d637d1b8771767918f5ce6615913`  
		Last Modified: Wed, 13 Nov 2024 14:36:26 GMT  
		Size: 10.9 MB (10871790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507e56710947c4dd3083f67fa34456eebb4c6bdbc143ba341e3fa55b672d5fd`  
		Last Modified: Fri, 15 Nov 2024 23:16:10 GMT  
		Size: 113.8 MB (113798721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2590da70ea99acbc45c33af0e63690eb64eda91a739b149685146e26ac689ce1`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101` - unknown; unknown

```console
$ docker pull ghost@sha256:51a79a847028b42640232a4f0cb52fcf6d3f8286a7712d64851558161d92ecfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465b25b619a2a59b8f9f8717ecd23e5ede5152d85c880b749e6729516c043878`

```dockerfile
```

-	Layers:
	-	`sha256:041a408bdcfb53782faf4553286f62b37627a0eda1c6dba47432c696f450baac`  
		Last Modified: Fri, 15 Nov 2024 23:16:07 GMT  
		Size: 5.4 MB (5442051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3210eb1fa6df8628b4aeb6e0f361960031cd81866b9c0cc1cffde16951feaae2`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b5de05b12149bc0e70c6d198a1355329773d651e789685c7312e3893ed9f84e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175855658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542706cc8f6ef6147c674b68fbc870bf5398117d8c1aacf6ef7efc7135fe9341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd83c78bbcfdd59177d67cdf89d1ccebb974e65ce433046486c1e297458a71`  
		Last Modified: Mon, 18 Nov 2024 16:57:30 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f209b7eb95422a153127b9a38a0d045d24287397e8b9d9ae3200442bf75d274`  
		Last Modified: Mon, 18 Nov 2024 17:44:45 GMT  
		Size: 38.3 MB (38304628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33194ef90e970e5976ac687ef339159661c5eb2e65c8d475bce213c9203dec7f`  
		Last Modified: Mon, 18 Nov 2024 17:44:44 GMT  
		Size: 1.7 MB (1712458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd4d3676c518b3a1b588c15c6b3ce261adb6d213780a32d8f17d15ad402edc`  
		Last Modified: Mon, 18 Nov 2024 17:44:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa547ff5f4f418b328c42bf29a767b530aaf653cc22e28dd01bf076a574d6a`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 1.4 MB (1376512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40471a53cff3131aa22de8b8b09c60f08cfce29c6da815937a5f21551cafd64`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 10.9 MB (10886537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4925238f229c0ab8be0f43f06953c20cff33a3f7d651c1dfb96b1762ed18a4`  
		Last Modified: Mon, 18 Nov 2024 17:49:43 GMT  
		Size: 94.4 MB (94413827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ecaa1d170551cc46d629ca7442cc310db1f24a4f2fa6cb5cb1e2eb8e594ff0`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101` - unknown; unknown

```console
$ docker pull ghost@sha256:21dd101fc39119378c1617a26e3adf62b6c436548c9e92ded338f99d6e59b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d0ca1207a5253ad06d841fb27cc82d1734673cf09c1299872ccd59e7288ffe`

```dockerfile
```

-	Layers:
	-	`sha256:2f04b8e6d88b44b2409a14eee8b3d5a81d47e27699755107c93ecae166e7563b`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 5.4 MB (5431472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92259aae7eb20f16ca913b4a047a10ea4ccffb609db397f834a6bb8e1213aaa2`  
		Last Modified: Mon, 18 Nov 2024 17:49:39 GMT  
		Size: 29.4 KB (29440 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101` - linux; ppc64le

```console
$ docker pull ghost@sha256:a42d82e08f68045aac512d8a90b3cb43717affe18810b776ee5a218338dbddb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188438582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217979c19dc7b34eba5e3abde0ff4bb5b5a5db88a038315cf4341d773b0e55c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b818420b8b420d93637d67bd46b71029bfb1e062b744b14c8f79e7a7cb6589`  
		Last Modified: Tue, 12 Nov 2024 09:03:45 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d859570a00ca2b65000799fc1cdd091706ff08e28882bd44d6d6d3152e20c`  
		Last Modified: Mon, 18 Nov 2024 15:41:14 GMT  
		Size: 40.4 MB (40351609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8924ec273e919caf7a8a1210fc8992a235b183678e7686dd941b3f295287a`  
		Last Modified: Mon, 18 Nov 2024 15:41:13 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b1adc6ea76ee1a63da85d99c948134d2f3a81ea73d7383aa5e8c3878cc1e5`  
		Last Modified: Mon, 18 Nov 2024 15:41:12 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d34ba125482343643488b81300b7f2ce0aed0c6695145a848c73f0925e5e2`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 1.4 MB (1366618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86e8cffb2db3795823e0a1b7a686bd540c5d02918ef232ca6173d60e2c82c1f`  
		Last Modified: Mon, 18 Nov 2024 15:57:45 GMT  
		Size: 10.9 MB (10890010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff12d6c364e7c870226185011eda5f11ab082357b9d1e1f1fc7083807a1491`  
		Last Modified: Mon, 18 Nov 2024 15:57:49 GMT  
		Size: 101.0 MB (100987987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0da1180f914637f06b82c1be6eaeda13df6c62142bd6bc7c25026bbb9c921f0`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101` - unknown; unknown

```console
$ docker pull ghost@sha256:9e5841ed29ecc752e24909d28f52d776a7cb08c5ea10a5ecdafbf943f4e085cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7b4e806e2e543eb2b07196bd3deca075e913024cb28376da6205288ce17b96`

```dockerfile
```

-	Layers:
	-	`sha256:a930f663b0655f899dc638f1eda5b9af40fda08089b78bc0e5697cf4b1a77277`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 5.4 MB (5427476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce245dd38ad15f6264d37c3569780606360fb353c9f27db162b6229a8c224c0b`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 29.4 KB (29358 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101` - linux; s390x

```console
$ docker pull ghost@sha256:a326c789845b43e67fd70ea192992d31dcf818df5fd6767ef7dda74b8223dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180850920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7be82c62dbd13412005728f285f630b21a101f86d5e0c8e37222f0422d35a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5936a9967200e38b9edc3158d32d0bd35fcdadb6ce24041a0fd1a4c31f82bac`  
		Last Modified: Tue, 12 Nov 2024 12:15:56 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34127b12d15850d7834b1077b8c55b769151447e9c26ef585c832e35d5caa0f4`  
		Last Modified: Tue, 12 Nov 2024 17:32:29 GMT  
		Size: 38.4 MB (38403967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682b50f1b1c57d9a4cc8e4b2569ee33bf7d2c5afd57964c5efc69d5bb09df5bb`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 1.7 MB (1708311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068d72d677c3a3b185ce6bb3b5db7e1eb7b1ebd26d8ab52bcff4d7ed2bf6693`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e40c0afde1ff131a4380bd2bb16012712b2bb9b091b56f14888438f693baecc`  
		Last Modified: Wed, 13 Nov 2024 02:22:49 GMT  
		Size: 1.4 MB (1410261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f92cb1aeadc76a8e91374dca4bf3f04465601adbea07f9aa36d57660d4895`  
		Last Modified: Wed, 13 Nov 2024 02:22:50 GMT  
		Size: 10.9 MB (10869645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e6a2863f96037bb86576689a3dd515773e4b3d43e3e4e33ada9ea731e079b2`  
		Last Modified: Sat, 16 Nov 2024 00:10:10 GMT  
		Size: 101.0 MB (100962775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce9224d49b17f4577f5291a40b93f3b124466f532d43090377266a1de80ca62`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101` - unknown; unknown

```console
$ docker pull ghost@sha256:cbd04823c522f5a854665ce8382f3324c65be685bc14e2b857e44a699be89ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131f693be06516c73c7409d0b3f78cf906d14b077cfed59b642f240f8965d7dc`

```dockerfile
```

-	Layers:
	-	`sha256:e4c0e1beb4eddfc2be9cbc018f270692a545b3f1dacd08ad645ed806cacc7699`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 5.4 MB (5428310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcc27429a3bcb37b1d410f808d89f1e0f11e5f4c2ee74903451f87ec39a059a`  
		Last Modified: Sat, 16 Nov 2024 00:10:06 GMT  
		Size: 29.3 KB (29310 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.101-alpine`

```console
$ docker pull ghost@sha256:18374c65f40ddadd1891e8d7a5ad2c5194248d1cb4c18772a367b7fd2e8ca536
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

### `ghost:5.101-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1f1f74109cbbd5ee6c39119f01c3f02c4d9273d45045dab12b95b879d522429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148314439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87f98b1fd1ac9710b0d618841c05141ac97c528da4a1b6963891198c256df26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5ba5322b4a5416240b08583db88aae9b9138dd36fd54aa9d20173c3db57851`  
		Last Modified: Mon, 18 Nov 2024 15:04:48 GMT  
		Size: 40.1 MB (40091144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c4a69072cc1e5ba000ae076927371dc1d755805dfc729ae27814d9b8ada2f`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36d32de04200f805172fdaa1bbe7a28053ec150a9b4cc181803fa3f44d8be09`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304a60e90041b1cc9cd91553b7d697e15550e292740c3c76794b9621805f775`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 776.0 KB (776023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dee8aec1a555510b06e12d3cd69c471ab3fe1cb9f7b7db63bb11ce05dcebce`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 1.1 MB (1121665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9475f3353914e8da3bea48022acf27cc5603b7e79b3b73a7bf897ab53c28acd`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca8aae3943880c5677429fe4aec791aa311a7d03a63469ffb68278f13a1288`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 10.9 MB (10885270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c6f70ce981c85a6364b736b6fc34a760ddc039646a5e7c88603b780e0be394`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 90.6 MB (90632188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9bc7a5daee07471c168be1fe888dabab39cf0ae559f10f16bd5ed9497c23e`  
		Last Modified: Mon, 18 Nov 2024 15:49:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:505c3b5912be58a3e1f08b24623deca7afa7464dbe75ff5c939138602671cbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dfc73487013b4de2d77c00840acbd4aba06541c4e6cff3adc101148902cf58`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa258f4ef14668447ba76bf7472321c92ee4b6cd005cd3d507a65a672d714a`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 3.3 MB (3322041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3805ec0ea0654b419ccb3f4ede0e8a2cb4373f41b4abf86476af5de88e7635`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 32.2 KB (32246 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:238949b177213fd865adc8667c565246c683e32a1b3d09f387193826050237d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154792064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a61a3d99ddf4c68cb84b5f0ffcd8609b88b2bc32178adba3e8724ace7bc7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5303b3afb218972eabf2203cb43b270ec96e28d49e0910900b0454f7cd15ad`  
		Last Modified: Tue, 12 Nov 2024 13:13:47 GMT  
		Size: 38.4 MB (38420266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac520e29cdd00b18e0a99c1da3851dc793f477a23eb22c051090e229318e9d9e`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 1.4 MB (1382250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e1218025d1d9d0b50ce6a18083d3642e07564c09f946fe7ccac4af14d1cd72`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12878dac288d46e798fc65b46ffc0069f31dd9d62fe3c28c3036e81fdf370daa`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 767.8 KB (767849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb19f8ebb4e341a0b72450e667b8518b41c8d12e44b365b7845cf7473064463a`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 1.1 MB (1088936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327b34e6e3bc78353d642c4f368171cb7245701de1a3df520dbbcd6dbdf68930`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a8ac45478fbffdd11d363cc812684b0f9a47263252425c064dda1291690388`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 10.9 MB (10887483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf4470a8e65453783ef724279c83670f49eb5d0f804f9ea9a69bf65fc673c9`  
		Last Modified: Fri, 15 Nov 2024 23:19:10 GMT  
		Size: 99.1 MB (99067660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d71695876930af3fedcc44df4cc38ceae365216e344959f6848d0542eafbfc`  
		Last Modified: Fri, 15 Nov 2024 23:19:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2b4e8c448f26e1243d430fa2396d99982df1995e9a03707161580b8871710242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6074401562c738383fdea6871eeb2debe8a1ff0e186b2f109c3b42ba0f15a`

```dockerfile
```

-	Layers:
	-	`sha256:548cda8cd16e4cfd1f9fa406331ffc0ed4233b7e3f35f8acf1128852a3ef4333`  
		Last Modified: Fri, 15 Nov 2024 23:19:06 GMT  
		Size: 32.2 KB (32158 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b08439262a81da78fabb8c34d8a635c9c78c301c18b5e9d41ded7c4014096afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153652792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ffff1aebc7d8da4d09f032cf3fc23665fa6d25cf09f71ac53329ab27ef997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace86978619da2f36047b5cbdbd518e2f3981dd44cf545695c7e7d04170442d1`  
		Last Modified: Tue, 12 Nov 2024 23:21:38 GMT  
		Size: 37.9 MB (37925094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8250d0c0ebf3e9e5be6339bacf03360dc4fa1b5b0fe6a7c9aa916d91d959e`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 1.4 MB (1382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46313ae619e2b3cd9b20ce8d6ccf91e56398fc35c81a19b69d3253a68af4f7da`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fb97108fad0c6fff92bf6e507d46e7dc4fb65661e50bc0733747b6ad1a667`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 701.2 KB (701151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ddaedc2788cd21ed9d5e9fcfc09d0f7145966762d8e39a293dd79e08bb5678`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 1.1 MB (1088905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1473a48abffd7c0eeb6a49dd88b9bf462c7cbb152fd068c095b6a8698da30`  
		Last Modified: Wed, 13 Nov 2024 14:46:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f89d31231794101e907fc69b00faec60df311f773eaecec1a05b91a35bbdce`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 10.9 MB (10871426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7a993d59db0b8ed2785fb42f58f35171c3228b1bcb1a48127127aa82114169`  
		Last Modified: Fri, 15 Nov 2024 23:25:57 GMT  
		Size: 98.8 MB (98755042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248b6c06ec8bcc232e75f32d5b24d4b19c2c9afb5723b75bf30627887dfc3ae`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:297f563b7714786a047939e69d35cbb6626ff07fbf88ff64526bac71c8651ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb1a4d37cfe9cafb4de39ca3a20eeb8f3fafe7c2f54491086767403a508e109`

```dockerfile
```

-	Layers:
	-	`sha256:506ac704993e74231440f52fbe50e21974d6e78e56df1d20659110aaaeab187d`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 3.3 MB (3319434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b34d600e500f16220aaf2c7753747f3c78d677c83e3d3d9342f71ec7292bd`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 32.4 KB (32374 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:bd40723939738d573d37193256e92964575db0e07b966dfd1688f13d9f1957b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167814019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81b595fbfba87ae253192ed5f2ee9410f325db1370a7e75483261775b99d8da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145d210cb54045f3c727468bf465a3f263ff707a64da19e7d5d7f39680534637`  
		Last Modified: Mon, 18 Nov 2024 17:21:20 GMT  
		Size: 39.6 MB (39614415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc6f17d6ed2208b0d690e9e6ca3e3704177f4bbf02182a206951021f7b401c`  
		Last Modified: Mon, 18 Nov 2024 17:21:19 GMT  
		Size: 1.4 MB (1387220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628a8cd3385e1d2063448f845b9b3f70a2834e0ceb45f5e0a035e2a39d5e51bc`  
		Last Modified: Mon, 18 Nov 2024 17:21:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fba904282f0ae4661eb40bb1a336279a8c7e9af817034c5145a8deca9cb58f`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 852.8 KB (852762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd011e73ee54d748bee7de6a4a9974a246cd5f72ca059ee99d4405759745cd40`  
		Last Modified: Mon, 18 Nov 2024 17:53:34 GMT  
		Size: 1.1 MB (1053459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d41d78063ef9e70d23b6438b16eed5d96517c0b78d730e6cffac2906ce4ac`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8b461b47a202bfbff2e5bedeb7e7bcd04c07a03a67abc603096088efb14d1`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 10.9 MB (10886849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26d62a97f1c90f865c67eab88a3a756ca08e055df223e6bcc8024d5d7cfe4d`  
		Last Modified: Mon, 18 Nov 2024 17:53:37 GMT  
		Size: 110.7 MB (110658882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fec79d6636ddbbcf6e0e192d19455a1634867415f35b3198b09c8aa685556`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ccbd6f0e337395587e428bd68e0974485847d3962c52a31fcac0bd807edb6aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc5a3ba93c431b889aad9e2b05d9e865d3b6fbc4173909b3517105f8b58268d`

```dockerfile
```

-	Layers:
	-	`sha256:84ffb304164ac8a02b781b4d307175e2ec11a8f58cd3f1efc8b962ece4b7daee`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 3.3 MB (3322097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330334c78d29fe9ee2f7771ed9599d6db5efe037b9e9ddf7f965f05365f5322e`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 32.4 KB (32411 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.101.1`

```console
$ docker pull ghost@sha256:93ff4c2dda1531782a52175fd42cdd3a278c318d6b8c897af737eb06acfd62b1
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

### `ghost:5.101.1` - linux; amd64

```console
$ docker pull ghost@sha256:6adda1218d7db5552dff86974609220c47c5b42455877758bf771833acbe90a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174858883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e767e7d7923b8919bcf7a828a89c0363dbf0511857c5954add8c4029cee2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1a8e62161bc0632b3015ed29f3acd39ad51967b9f520b7fbca4b87d4abbfc`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a420fb4222f0ca00745cba1f93c448edc40483577dd3293abc23411009bb5c`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 38.2 MB (38233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e947ca9116f18eee431341298f0ae84403e13b359264a10d8358cf4766fbb0`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 1.7 MB (1712393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651c84feb4c5f72324ad867e61b43fbe28a681bd83493219a6dba60cf1dbf6`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15990d70afcacd012de19dc75538eafb360d11efdfe9676262b2a856755c31f`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 1.4 MB (1444746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be436f9b3739a5ed1c8a35370b8428efdabafb812bca44a69d8e98a2b518dc52`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 10.9 MB (10886453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d542188c5707d31aeb0f29119b5baa3b7c4dd84695779828ffc1571c2054e`  
		Last Modified: Mon, 18 Nov 2024 15:49:33 GMT  
		Size: 93.4 MB (93449346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29ef52eff3cfe8671ca39667c8b9f1a3b5c24acfcf4e4f98c081fbafdf495a`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1` - unknown; unknown

```console
$ docker pull ghost@sha256:668435a744e259d426d0e29c09881d1c2060ebb677e4312277bd2c20c07cf3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a631f2c2445e543838043b99b674ca785c498c5678645c03dd54681b335b29f3`

```dockerfile
```

-	Layers:
	-	`sha256:faecc37e3bfb421e312d7e910108ef0ca5b430f410ea358ff7b580c156e04681`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 5.4 MB (5431222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6686300074dd68d5356dc3d9811ffb58ae4161d8c18e14d37801c2cb2ee078`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fdba2da346f989ded93d0381a78b52b953826757e88cd44f073ba2c2b6aa7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187348764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa26e0ac62ed60d585437970be8cd16770d9dd3a837e0310558dcf98f3b84e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12e8f4279bfa57e91b124afb54540f003f2bca339945f6a92e0fe2521df05e`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c10b5c43ca02ec06641a0ecab5bbe328afe13154fd9b2d5b07c2b1e5dd31c4`  
		Last Modified: Tue, 12 Nov 2024 23:46:57 GMT  
		Size: 34.8 MB (34834213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb1880d4b7c1d0c9cc7a18adbafb6d5c0dc15fe9ecc0963d0acebbdd5dd54a`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 1.7 MB (1708399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f51d33dfbc7d2eff0b37c55149300e299820a5b3dc556b8879f773c0f928741`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121220baf3c300e0dd3aa98a69e6532d9d7bc0595f7457cba1fe3f0d60e0f9c`  
		Last Modified: Wed, 13 Nov 2024 14:36:25 GMT  
		Size: 1.4 MB (1412399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a2999a7a218d7e7db282d9394133403e8d637d1b8771767918f5ce6615913`  
		Last Modified: Wed, 13 Nov 2024 14:36:26 GMT  
		Size: 10.9 MB (10871790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507e56710947c4dd3083f67fa34456eebb4c6bdbc143ba341e3fa55b672d5fd`  
		Last Modified: Fri, 15 Nov 2024 23:16:10 GMT  
		Size: 113.8 MB (113798721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2590da70ea99acbc45c33af0e63690eb64eda91a739b149685146e26ac689ce1`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1` - unknown; unknown

```console
$ docker pull ghost@sha256:51a79a847028b42640232a4f0cb52fcf6d3f8286a7712d64851558161d92ecfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465b25b619a2a59b8f9f8717ecd23e5ede5152d85c880b749e6729516c043878`

```dockerfile
```

-	Layers:
	-	`sha256:041a408bdcfb53782faf4553286f62b37627a0eda1c6dba47432c696f450baac`  
		Last Modified: Fri, 15 Nov 2024 23:16:07 GMT  
		Size: 5.4 MB (5442051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3210eb1fa6df8628b4aeb6e0f361960031cd81866b9c0cc1cffde16951feaae2`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b5de05b12149bc0e70c6d198a1355329773d651e789685c7312e3893ed9f84e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175855658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542706cc8f6ef6147c674b68fbc870bf5398117d8c1aacf6ef7efc7135fe9341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd83c78bbcfdd59177d67cdf89d1ccebb974e65ce433046486c1e297458a71`  
		Last Modified: Mon, 18 Nov 2024 16:57:30 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f209b7eb95422a153127b9a38a0d045d24287397e8b9d9ae3200442bf75d274`  
		Last Modified: Mon, 18 Nov 2024 17:44:45 GMT  
		Size: 38.3 MB (38304628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33194ef90e970e5976ac687ef339159661c5eb2e65c8d475bce213c9203dec7f`  
		Last Modified: Mon, 18 Nov 2024 17:44:44 GMT  
		Size: 1.7 MB (1712458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd4d3676c518b3a1b588c15c6b3ce261adb6d213780a32d8f17d15ad402edc`  
		Last Modified: Mon, 18 Nov 2024 17:44:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa547ff5f4f418b328c42bf29a767b530aaf653cc22e28dd01bf076a574d6a`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 1.4 MB (1376512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40471a53cff3131aa22de8b8b09c60f08cfce29c6da815937a5f21551cafd64`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 10.9 MB (10886537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4925238f229c0ab8be0f43f06953c20cff33a3f7d651c1dfb96b1762ed18a4`  
		Last Modified: Mon, 18 Nov 2024 17:49:43 GMT  
		Size: 94.4 MB (94413827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ecaa1d170551cc46d629ca7442cc310db1f24a4f2fa6cb5cb1e2eb8e594ff0`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1` - unknown; unknown

```console
$ docker pull ghost@sha256:21dd101fc39119378c1617a26e3adf62b6c436548c9e92ded338f99d6e59b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d0ca1207a5253ad06d841fb27cc82d1734673cf09c1299872ccd59e7288ffe`

```dockerfile
```

-	Layers:
	-	`sha256:2f04b8e6d88b44b2409a14eee8b3d5a81d47e27699755107c93ecae166e7563b`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 5.4 MB (5431472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92259aae7eb20f16ca913b4a047a10ea4ccffb609db397f834a6bb8e1213aaa2`  
		Last Modified: Mon, 18 Nov 2024 17:49:39 GMT  
		Size: 29.4 KB (29440 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1` - linux; ppc64le

```console
$ docker pull ghost@sha256:a42d82e08f68045aac512d8a90b3cb43717affe18810b776ee5a218338dbddb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188438582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217979c19dc7b34eba5e3abde0ff4bb5b5a5db88a038315cf4341d773b0e55c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b818420b8b420d93637d67bd46b71029bfb1e062b744b14c8f79e7a7cb6589`  
		Last Modified: Tue, 12 Nov 2024 09:03:45 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d859570a00ca2b65000799fc1cdd091706ff08e28882bd44d6d6d3152e20c`  
		Last Modified: Mon, 18 Nov 2024 15:41:14 GMT  
		Size: 40.4 MB (40351609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8924ec273e919caf7a8a1210fc8992a235b183678e7686dd941b3f295287a`  
		Last Modified: Mon, 18 Nov 2024 15:41:13 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b1adc6ea76ee1a63da85d99c948134d2f3a81ea73d7383aa5e8c3878cc1e5`  
		Last Modified: Mon, 18 Nov 2024 15:41:12 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d34ba125482343643488b81300b7f2ce0aed0c6695145a848c73f0925e5e2`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 1.4 MB (1366618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86e8cffb2db3795823e0a1b7a686bd540c5d02918ef232ca6173d60e2c82c1f`  
		Last Modified: Mon, 18 Nov 2024 15:57:45 GMT  
		Size: 10.9 MB (10890010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff12d6c364e7c870226185011eda5f11ab082357b9d1e1f1fc7083807a1491`  
		Last Modified: Mon, 18 Nov 2024 15:57:49 GMT  
		Size: 101.0 MB (100987987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0da1180f914637f06b82c1be6eaeda13df6c62142bd6bc7c25026bbb9c921f0`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1` - unknown; unknown

```console
$ docker pull ghost@sha256:9e5841ed29ecc752e24909d28f52d776a7cb08c5ea10a5ecdafbf943f4e085cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7b4e806e2e543eb2b07196bd3deca075e913024cb28376da6205288ce17b96`

```dockerfile
```

-	Layers:
	-	`sha256:a930f663b0655f899dc638f1eda5b9af40fda08089b78bc0e5697cf4b1a77277`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 5.4 MB (5427476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce245dd38ad15f6264d37c3569780606360fb353c9f27db162b6229a8c224c0b`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 29.4 KB (29358 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1` - linux; s390x

```console
$ docker pull ghost@sha256:a326c789845b43e67fd70ea192992d31dcf818df5fd6767ef7dda74b8223dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180850920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7be82c62dbd13412005728f285f630b21a101f86d5e0c8e37222f0422d35a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5936a9967200e38b9edc3158d32d0bd35fcdadb6ce24041a0fd1a4c31f82bac`  
		Last Modified: Tue, 12 Nov 2024 12:15:56 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34127b12d15850d7834b1077b8c55b769151447e9c26ef585c832e35d5caa0f4`  
		Last Modified: Tue, 12 Nov 2024 17:32:29 GMT  
		Size: 38.4 MB (38403967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682b50f1b1c57d9a4cc8e4b2569ee33bf7d2c5afd57964c5efc69d5bb09df5bb`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 1.7 MB (1708311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068d72d677c3a3b185ce6bb3b5db7e1eb7b1ebd26d8ab52bcff4d7ed2bf6693`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e40c0afde1ff131a4380bd2bb16012712b2bb9b091b56f14888438f693baecc`  
		Last Modified: Wed, 13 Nov 2024 02:22:49 GMT  
		Size: 1.4 MB (1410261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f92cb1aeadc76a8e91374dca4bf3f04465601adbea07f9aa36d57660d4895`  
		Last Modified: Wed, 13 Nov 2024 02:22:50 GMT  
		Size: 10.9 MB (10869645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e6a2863f96037bb86576689a3dd515773e4b3d43e3e4e33ada9ea731e079b2`  
		Last Modified: Sat, 16 Nov 2024 00:10:10 GMT  
		Size: 101.0 MB (100962775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce9224d49b17f4577f5291a40b93f3b124466f532d43090377266a1de80ca62`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1` - unknown; unknown

```console
$ docker pull ghost@sha256:cbd04823c522f5a854665ce8382f3324c65be685bc14e2b857e44a699be89ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131f693be06516c73c7409d0b3f78cf906d14b077cfed59b642f240f8965d7dc`

```dockerfile
```

-	Layers:
	-	`sha256:e4c0e1beb4eddfc2be9cbc018f270692a545b3f1dacd08ad645ed806cacc7699`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 5.4 MB (5428310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcc27429a3bcb37b1d410f808d89f1e0f11e5f4c2ee74903451f87ec39a059a`  
		Last Modified: Sat, 16 Nov 2024 00:10:06 GMT  
		Size: 29.3 KB (29310 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.101.1-alpine`

```console
$ docker pull ghost@sha256:18374c65f40ddadd1891e8d7a5ad2c5194248d1cb4c18772a367b7fd2e8ca536
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

### `ghost:5.101.1-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1f1f74109cbbd5ee6c39119f01c3f02c4d9273d45045dab12b95b879d522429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148314439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87f98b1fd1ac9710b0d618841c05141ac97c528da4a1b6963891198c256df26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5ba5322b4a5416240b08583db88aae9b9138dd36fd54aa9d20173c3db57851`  
		Last Modified: Mon, 18 Nov 2024 15:04:48 GMT  
		Size: 40.1 MB (40091144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c4a69072cc1e5ba000ae076927371dc1d755805dfc729ae27814d9b8ada2f`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36d32de04200f805172fdaa1bbe7a28053ec150a9b4cc181803fa3f44d8be09`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304a60e90041b1cc9cd91553b7d697e15550e292740c3c76794b9621805f775`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 776.0 KB (776023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dee8aec1a555510b06e12d3cd69c471ab3fe1cb9f7b7db63bb11ce05dcebce`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 1.1 MB (1121665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9475f3353914e8da3bea48022acf27cc5603b7e79b3b73a7bf897ab53c28acd`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca8aae3943880c5677429fe4aec791aa311a7d03a63469ffb68278f13a1288`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 10.9 MB (10885270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c6f70ce981c85a6364b736b6fc34a760ddc039646a5e7c88603b780e0be394`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 90.6 MB (90632188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9bc7a5daee07471c168be1fe888dabab39cf0ae559f10f16bd5ed9497c23e`  
		Last Modified: Mon, 18 Nov 2024 15:49:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:505c3b5912be58a3e1f08b24623deca7afa7464dbe75ff5c939138602671cbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dfc73487013b4de2d77c00840acbd4aba06541c4e6cff3adc101148902cf58`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa258f4ef14668447ba76bf7472321c92ee4b6cd005cd3d507a65a672d714a`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 3.3 MB (3322041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3805ec0ea0654b419ccb3f4ede0e8a2cb4373f41b4abf86476af5de88e7635`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 32.2 KB (32246 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:238949b177213fd865adc8667c565246c683e32a1b3d09f387193826050237d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154792064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a61a3d99ddf4c68cb84b5f0ffcd8609b88b2bc32178adba3e8724ace7bc7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5303b3afb218972eabf2203cb43b270ec96e28d49e0910900b0454f7cd15ad`  
		Last Modified: Tue, 12 Nov 2024 13:13:47 GMT  
		Size: 38.4 MB (38420266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac520e29cdd00b18e0a99c1da3851dc793f477a23eb22c051090e229318e9d9e`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 1.4 MB (1382250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e1218025d1d9d0b50ce6a18083d3642e07564c09f946fe7ccac4af14d1cd72`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12878dac288d46e798fc65b46ffc0069f31dd9d62fe3c28c3036e81fdf370daa`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 767.8 KB (767849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb19f8ebb4e341a0b72450e667b8518b41c8d12e44b365b7845cf7473064463a`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 1.1 MB (1088936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327b34e6e3bc78353d642c4f368171cb7245701de1a3df520dbbcd6dbdf68930`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a8ac45478fbffdd11d363cc812684b0f9a47263252425c064dda1291690388`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 10.9 MB (10887483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf4470a8e65453783ef724279c83670f49eb5d0f804f9ea9a69bf65fc673c9`  
		Last Modified: Fri, 15 Nov 2024 23:19:10 GMT  
		Size: 99.1 MB (99067660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d71695876930af3fedcc44df4cc38ceae365216e344959f6848d0542eafbfc`  
		Last Modified: Fri, 15 Nov 2024 23:19:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2b4e8c448f26e1243d430fa2396d99982df1995e9a03707161580b8871710242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6074401562c738383fdea6871eeb2debe8a1ff0e186b2f109c3b42ba0f15a`

```dockerfile
```

-	Layers:
	-	`sha256:548cda8cd16e4cfd1f9fa406331ffc0ed4233b7e3f35f8acf1128852a3ef4333`  
		Last Modified: Fri, 15 Nov 2024 23:19:06 GMT  
		Size: 32.2 KB (32158 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b08439262a81da78fabb8c34d8a635c9c78c301c18b5e9d41ded7c4014096afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153652792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ffff1aebc7d8da4d09f032cf3fc23665fa6d25cf09f71ac53329ab27ef997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace86978619da2f36047b5cbdbd518e2f3981dd44cf545695c7e7d04170442d1`  
		Last Modified: Tue, 12 Nov 2024 23:21:38 GMT  
		Size: 37.9 MB (37925094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8250d0c0ebf3e9e5be6339bacf03360dc4fa1b5b0fe6a7c9aa916d91d959e`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 1.4 MB (1382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46313ae619e2b3cd9b20ce8d6ccf91e56398fc35c81a19b69d3253a68af4f7da`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fb97108fad0c6fff92bf6e507d46e7dc4fb65661e50bc0733747b6ad1a667`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 701.2 KB (701151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ddaedc2788cd21ed9d5e9fcfc09d0f7145966762d8e39a293dd79e08bb5678`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 1.1 MB (1088905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1473a48abffd7c0eeb6a49dd88b9bf462c7cbb152fd068c095b6a8698da30`  
		Last Modified: Wed, 13 Nov 2024 14:46:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f89d31231794101e907fc69b00faec60df311f773eaecec1a05b91a35bbdce`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 10.9 MB (10871426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7a993d59db0b8ed2785fb42f58f35171c3228b1bcb1a48127127aa82114169`  
		Last Modified: Fri, 15 Nov 2024 23:25:57 GMT  
		Size: 98.8 MB (98755042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248b6c06ec8bcc232e75f32d5b24d4b19c2c9afb5723b75bf30627887dfc3ae`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:297f563b7714786a047939e69d35cbb6626ff07fbf88ff64526bac71c8651ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb1a4d37cfe9cafb4de39ca3a20eeb8f3fafe7c2f54491086767403a508e109`

```dockerfile
```

-	Layers:
	-	`sha256:506ac704993e74231440f52fbe50e21974d6e78e56df1d20659110aaaeab187d`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 3.3 MB (3319434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b34d600e500f16220aaf2c7753747f3c78d677c83e3d3d9342f71ec7292bd`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 32.4 KB (32374 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.101.1-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:bd40723939738d573d37193256e92964575db0e07b966dfd1688f13d9f1957b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167814019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81b595fbfba87ae253192ed5f2ee9410f325db1370a7e75483261775b99d8da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145d210cb54045f3c727468bf465a3f263ff707a64da19e7d5d7f39680534637`  
		Last Modified: Mon, 18 Nov 2024 17:21:20 GMT  
		Size: 39.6 MB (39614415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc6f17d6ed2208b0d690e9e6ca3e3704177f4bbf02182a206951021f7b401c`  
		Last Modified: Mon, 18 Nov 2024 17:21:19 GMT  
		Size: 1.4 MB (1387220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628a8cd3385e1d2063448f845b9b3f70a2834e0ceb45f5e0a035e2a39d5e51bc`  
		Last Modified: Mon, 18 Nov 2024 17:21:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fba904282f0ae4661eb40bb1a336279a8c7e9af817034c5145a8deca9cb58f`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 852.8 KB (852762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd011e73ee54d748bee7de6a4a9974a246cd5f72ca059ee99d4405759745cd40`  
		Last Modified: Mon, 18 Nov 2024 17:53:34 GMT  
		Size: 1.1 MB (1053459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d41d78063ef9e70d23b6438b16eed5d96517c0b78d730e6cffac2906ce4ac`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8b461b47a202bfbff2e5bedeb7e7bcd04c07a03a67abc603096088efb14d1`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 10.9 MB (10886849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26d62a97f1c90f865c67eab88a3a756ca08e055df223e6bcc8024d5d7cfe4d`  
		Last Modified: Mon, 18 Nov 2024 17:53:37 GMT  
		Size: 110.7 MB (110658882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fec79d6636ddbbcf6e0e192d19455a1634867415f35b3198b09c8aa685556`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.101.1-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ccbd6f0e337395587e428bd68e0974485847d3962c52a31fcac0bd807edb6aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc5a3ba93c431b889aad9e2b05d9e865d3b6fbc4173909b3517105f8b58268d`

```dockerfile
```

-	Layers:
	-	`sha256:84ffb304164ac8a02b781b4d307175e2ec11a8f58cd3f1efc8b962ece4b7daee`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 3.3 MB (3322097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330334c78d29fe9ee2f7771ed9599d6db5efe037b9e9ddf7f965f05365f5322e`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 32.4 KB (32411 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:18374c65f40ddadd1891e8d7a5ad2c5194248d1cb4c18772a367b7fd2e8ca536
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
$ docker pull ghost@sha256:1f1f74109cbbd5ee6c39119f01c3f02c4d9273d45045dab12b95b879d522429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148314439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87f98b1fd1ac9710b0d618841c05141ac97c528da4a1b6963891198c256df26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5ba5322b4a5416240b08583db88aae9b9138dd36fd54aa9d20173c3db57851`  
		Last Modified: Mon, 18 Nov 2024 15:04:48 GMT  
		Size: 40.1 MB (40091144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c4a69072cc1e5ba000ae076927371dc1d755805dfc729ae27814d9b8ada2f`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36d32de04200f805172fdaa1bbe7a28053ec150a9b4cc181803fa3f44d8be09`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304a60e90041b1cc9cd91553b7d697e15550e292740c3c76794b9621805f775`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 776.0 KB (776023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dee8aec1a555510b06e12d3cd69c471ab3fe1cb9f7b7db63bb11ce05dcebce`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 1.1 MB (1121665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9475f3353914e8da3bea48022acf27cc5603b7e79b3b73a7bf897ab53c28acd`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca8aae3943880c5677429fe4aec791aa311a7d03a63469ffb68278f13a1288`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 10.9 MB (10885270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c6f70ce981c85a6364b736b6fc34a760ddc039646a5e7c88603b780e0be394`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 90.6 MB (90632188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9bc7a5daee07471c168be1fe888dabab39cf0ae559f10f16bd5ed9497c23e`  
		Last Modified: Mon, 18 Nov 2024 15:49:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:505c3b5912be58a3e1f08b24623deca7afa7464dbe75ff5c939138602671cbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dfc73487013b4de2d77c00840acbd4aba06541c4e6cff3adc101148902cf58`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa258f4ef14668447ba76bf7472321c92ee4b6cd005cd3d507a65a672d714a`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 3.3 MB (3322041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3805ec0ea0654b419ccb3f4ede0e8a2cb4373f41b4abf86476af5de88e7635`  
		Last Modified: Mon, 18 Nov 2024 15:49:29 GMT  
		Size: 32.2 KB (32246 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:238949b177213fd865adc8667c565246c683e32a1b3d09f387193826050237d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154792064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a61a3d99ddf4c68cb84b5f0ffcd8609b88b2bc32178adba3e8724ace7bc7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5303b3afb218972eabf2203cb43b270ec96e28d49e0910900b0454f7cd15ad`  
		Last Modified: Tue, 12 Nov 2024 13:13:47 GMT  
		Size: 38.4 MB (38420266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac520e29cdd00b18e0a99c1da3851dc793f477a23eb22c051090e229318e9d9e`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 1.4 MB (1382250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e1218025d1d9d0b50ce6a18083d3642e07564c09f946fe7ccac4af14d1cd72`  
		Last Modified: Tue, 12 Nov 2024 13:13:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12878dac288d46e798fc65b46ffc0069f31dd9d62fe3c28c3036e81fdf370daa`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 767.8 KB (767849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb19f8ebb4e341a0b72450e667b8518b41c8d12e44b365b7845cf7473064463a`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 1.1 MB (1088936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327b34e6e3bc78353d642c4f368171cb7245701de1a3df520dbbcd6dbdf68930`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a8ac45478fbffdd11d363cc812684b0f9a47263252425c064dda1291690388`  
		Last Modified: Tue, 12 Nov 2024 17:37:29 GMT  
		Size: 10.9 MB (10887483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf4470a8e65453783ef724279c83670f49eb5d0f804f9ea9a69bf65fc673c9`  
		Last Modified: Fri, 15 Nov 2024 23:19:10 GMT  
		Size: 99.1 MB (99067660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d71695876930af3fedcc44df4cc38ceae365216e344959f6848d0542eafbfc`  
		Last Modified: Fri, 15 Nov 2024 23:19:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2b4e8c448f26e1243d430fa2396d99982df1995e9a03707161580b8871710242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6074401562c738383fdea6871eeb2debe8a1ff0e186b2f109c3b42ba0f15a`

```dockerfile
```

-	Layers:
	-	`sha256:548cda8cd16e4cfd1f9fa406331ffc0ed4233b7e3f35f8acf1128852a3ef4333`  
		Last Modified: Fri, 15 Nov 2024 23:19:06 GMT  
		Size: 32.2 KB (32158 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b08439262a81da78fabb8c34d8a635c9c78c301c18b5e9d41ded7c4014096afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153652792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ffff1aebc7d8da4d09f032cf3fc23665fa6d25cf09f71ac53329ab27ef997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace86978619da2f36047b5cbdbd518e2f3981dd44cf545695c7e7d04170442d1`  
		Last Modified: Tue, 12 Nov 2024 23:21:38 GMT  
		Size: 37.9 MB (37925094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8250d0c0ebf3e9e5be6339bacf03360dc4fa1b5b0fe6a7c9aa916d91d959e`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 1.4 MB (1382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46313ae619e2b3cd9b20ce8d6ccf91e56398fc35c81a19b69d3253a68af4f7da`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fb97108fad0c6fff92bf6e507d46e7dc4fb65661e50bc0733747b6ad1a667`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 701.2 KB (701151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ddaedc2788cd21ed9d5e9fcfc09d0f7145966762d8e39a293dd79e08bb5678`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 1.1 MB (1088905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1473a48abffd7c0eeb6a49dd88b9bf462c7cbb152fd068c095b6a8698da30`  
		Last Modified: Wed, 13 Nov 2024 14:46:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f89d31231794101e907fc69b00faec60df311f773eaecec1a05b91a35bbdce`  
		Last Modified: Wed, 13 Nov 2024 14:46:23 GMT  
		Size: 10.9 MB (10871426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7a993d59db0b8ed2785fb42f58f35171c3228b1bcb1a48127127aa82114169`  
		Last Modified: Fri, 15 Nov 2024 23:25:57 GMT  
		Size: 98.8 MB (98755042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248b6c06ec8bcc232e75f32d5b24d4b19c2c9afb5723b75bf30627887dfc3ae`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:297f563b7714786a047939e69d35cbb6626ff07fbf88ff64526bac71c8651ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb1a4d37cfe9cafb4de39ca3a20eeb8f3fafe7c2f54491086767403a508e109`

```dockerfile
```

-	Layers:
	-	`sha256:506ac704993e74231440f52fbe50e21974d6e78e56df1d20659110aaaeab187d`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 3.3 MB (3319434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b34d600e500f16220aaf2c7753747f3c78d677c83e3d3d9342f71ec7292bd`  
		Last Modified: Fri, 15 Nov 2024 23:25:54 GMT  
		Size: 32.4 KB (32374 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:bd40723939738d573d37193256e92964575db0e07b966dfd1688f13d9f1957b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167814019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81b595fbfba87ae253192ed5f2ee9410f325db1370a7e75483261775b99d8da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145d210cb54045f3c727468bf465a3f263ff707a64da19e7d5d7f39680534637`  
		Last Modified: Mon, 18 Nov 2024 17:21:20 GMT  
		Size: 39.6 MB (39614415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc6f17d6ed2208b0d690e9e6ca3e3704177f4bbf02182a206951021f7b401c`  
		Last Modified: Mon, 18 Nov 2024 17:21:19 GMT  
		Size: 1.4 MB (1387220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628a8cd3385e1d2063448f845b9b3f70a2834e0ceb45f5e0a035e2a39d5e51bc`  
		Last Modified: Mon, 18 Nov 2024 17:21:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fba904282f0ae4661eb40bb1a336279a8c7e9af817034c5145a8deca9cb58f`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 852.8 KB (852762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd011e73ee54d748bee7de6a4a9974a246cd5f72ca059ee99d4405759745cd40`  
		Last Modified: Mon, 18 Nov 2024 17:53:34 GMT  
		Size: 1.1 MB (1053459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d41d78063ef9e70d23b6438b16eed5d96517c0b78d730e6cffac2906ce4ac`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8b461b47a202bfbff2e5bedeb7e7bcd04c07a03a67abc603096088efb14d1`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 10.9 MB (10886849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26d62a97f1c90f865c67eab88a3a756ca08e055df223e6bcc8024d5d7cfe4d`  
		Last Modified: Mon, 18 Nov 2024 17:53:37 GMT  
		Size: 110.7 MB (110658882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fec79d6636ddbbcf6e0e192d19455a1634867415f35b3198b09c8aa685556`  
		Last Modified: Mon, 18 Nov 2024 17:53:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ccbd6f0e337395587e428bd68e0974485847d3962c52a31fcac0bd807edb6aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc5a3ba93c431b889aad9e2b05d9e865d3b6fbc4173909b3517105f8b58268d`

```dockerfile
```

-	Layers:
	-	`sha256:84ffb304164ac8a02b781b4d307175e2ec11a8f58cd3f1efc8b962ece4b7daee`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 3.3 MB (3322097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330334c78d29fe9ee2f7771ed9599d6db5efe037b9e9ddf7f965f05365f5322e`  
		Last Modified: Mon, 18 Nov 2024 17:53:33 GMT  
		Size: 32.4 KB (32411 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:93ff4c2dda1531782a52175fd42cdd3a278c318d6b8c897af737eb06acfd62b1
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
$ docker pull ghost@sha256:6adda1218d7db5552dff86974609220c47c5b42455877758bf771833acbe90a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174858883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e767e7d7923b8919bcf7a828a89c0363dbf0511857c5954add8c4029cee2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1a8e62161bc0632b3015ed29f3acd39ad51967b9f520b7fbca4b87d4abbfc`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a420fb4222f0ca00745cba1f93c448edc40483577dd3293abc23411009bb5c`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 38.2 MB (38233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e947ca9116f18eee431341298f0ae84403e13b359264a10d8358cf4766fbb0`  
		Last Modified: Mon, 18 Nov 2024 15:05:02 GMT  
		Size: 1.7 MB (1712393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651c84feb4c5f72324ad867e61b43fbe28a681bd83493219a6dba60cf1dbf6`  
		Last Modified: Mon, 18 Nov 2024 15:05:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15990d70afcacd012de19dc75538eafb360d11efdfe9676262b2a856755c31f`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 1.4 MB (1444746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be436f9b3739a5ed1c8a35370b8428efdabafb812bca44a69d8e98a2b518dc52`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 10.9 MB (10886453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d542188c5707d31aeb0f29119b5baa3b7c4dd84695779828ffc1571c2054e`  
		Last Modified: Mon, 18 Nov 2024 15:49:33 GMT  
		Size: 93.4 MB (93449346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29ef52eff3cfe8671ca39667c8b9f1a3b5c24acfcf4e4f98c081fbafdf495a`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:668435a744e259d426d0e29c09881d1c2060ebb677e4312277bd2c20c07cf3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a631f2c2445e543838043b99b674ca785c498c5678645c03dd54681b335b29f3`

```dockerfile
```

-	Layers:
	-	`sha256:faecc37e3bfb421e312d7e910108ef0ca5b430f410ea358ff7b580c156e04681`  
		Last Modified: Mon, 18 Nov 2024 15:49:32 GMT  
		Size: 5.4 MB (5431222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6686300074dd68d5356dc3d9811ffb58ae4161d8c18e14d37801c2cb2ee078`  
		Last Modified: Mon, 18 Nov 2024 15:49:31 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fdba2da346f989ded93d0381a78b52b953826757e88cd44f073ba2c2b6aa7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187348764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa26e0ac62ed60d585437970be8cd16770d9dd3a837e0310558dcf98f3b84e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12e8f4279bfa57e91b124afb54540f003f2bca339945f6a92e0fe2521df05e`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c10b5c43ca02ec06641a0ecab5bbe328afe13154fd9b2d5b07c2b1e5dd31c4`  
		Last Modified: Tue, 12 Nov 2024 23:46:57 GMT  
		Size: 34.8 MB (34834213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb1880d4b7c1d0c9cc7a18adbafb6d5c0dc15fe9ecc0963d0acebbdd5dd54a`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 1.7 MB (1708399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f51d33dfbc7d2eff0b37c55149300e299820a5b3dc556b8879f773c0f928741`  
		Last Modified: Tue, 12 Nov 2024 23:46:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121220baf3c300e0dd3aa98a69e6532d9d7bc0595f7457cba1fe3f0d60e0f9c`  
		Last Modified: Wed, 13 Nov 2024 14:36:25 GMT  
		Size: 1.4 MB (1412399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a2999a7a218d7e7db282d9394133403e8d637d1b8771767918f5ce6615913`  
		Last Modified: Wed, 13 Nov 2024 14:36:26 GMT  
		Size: 10.9 MB (10871790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507e56710947c4dd3083f67fa34456eebb4c6bdbc143ba341e3fa55b672d5fd`  
		Last Modified: Fri, 15 Nov 2024 23:16:10 GMT  
		Size: 113.8 MB (113798721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2590da70ea99acbc45c33af0e63690eb64eda91a739b149685146e26ac689ce1`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:51a79a847028b42640232a4f0cb52fcf6d3f8286a7712d64851558161d92ecfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465b25b619a2a59b8f9f8717ecd23e5ede5152d85c880b749e6729516c043878`

```dockerfile
```

-	Layers:
	-	`sha256:041a408bdcfb53782faf4553286f62b37627a0eda1c6dba47432c696f450baac`  
		Last Modified: Fri, 15 Nov 2024 23:16:07 GMT  
		Size: 5.4 MB (5442051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3210eb1fa6df8628b4aeb6e0f361960031cd81866b9c0cc1cffde16951feaae2`  
		Last Modified: Fri, 15 Nov 2024 23:16:06 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b5de05b12149bc0e70c6d198a1355329773d651e789685c7312e3893ed9f84e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175855658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542706cc8f6ef6147c674b68fbc870bf5398117d8c1aacf6ef7efc7135fe9341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd83c78bbcfdd59177d67cdf89d1ccebb974e65ce433046486c1e297458a71`  
		Last Modified: Mon, 18 Nov 2024 16:57:30 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f209b7eb95422a153127b9a38a0d045d24287397e8b9d9ae3200442bf75d274`  
		Last Modified: Mon, 18 Nov 2024 17:44:45 GMT  
		Size: 38.3 MB (38304628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33194ef90e970e5976ac687ef339159661c5eb2e65c8d475bce213c9203dec7f`  
		Last Modified: Mon, 18 Nov 2024 17:44:44 GMT  
		Size: 1.7 MB (1712458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd4d3676c518b3a1b588c15c6b3ce261adb6d213780a32d8f17d15ad402edc`  
		Last Modified: Mon, 18 Nov 2024 17:44:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa547ff5f4f418b328c42bf29a767b530aaf653cc22e28dd01bf076a574d6a`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 1.4 MB (1376512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40471a53cff3131aa22de8b8b09c60f08cfce29c6da815937a5f21551cafd64`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 10.9 MB (10886537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4925238f229c0ab8be0f43f06953c20cff33a3f7d651c1dfb96b1762ed18a4`  
		Last Modified: Mon, 18 Nov 2024 17:49:43 GMT  
		Size: 94.4 MB (94413827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ecaa1d170551cc46d629ca7442cc310db1f24a4f2fa6cb5cb1e2eb8e594ff0`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:21dd101fc39119378c1617a26e3adf62b6c436548c9e92ded338f99d6e59b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d0ca1207a5253ad06d841fb27cc82d1734673cf09c1299872ccd59e7288ffe`

```dockerfile
```

-	Layers:
	-	`sha256:2f04b8e6d88b44b2409a14eee8b3d5a81d47e27699755107c93ecae166e7563b`  
		Last Modified: Mon, 18 Nov 2024 17:49:40 GMT  
		Size: 5.4 MB (5431472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92259aae7eb20f16ca913b4a047a10ea4ccffb609db397f834a6bb8e1213aaa2`  
		Last Modified: Mon, 18 Nov 2024 17:49:39 GMT  
		Size: 29.4 KB (29440 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:a42d82e08f68045aac512d8a90b3cb43717affe18810b776ee5a218338dbddb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188438582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217979c19dc7b34eba5e3abde0ff4bb5b5a5db88a038315cf4341d773b0e55c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 21:19:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 21:19:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node"]
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b818420b8b420d93637d67bd46b71029bfb1e062b744b14c8f79e7a7cb6589`  
		Last Modified: Tue, 12 Nov 2024 09:03:45 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d859570a00ca2b65000799fc1cdd091706ff08e28882bd44d6d6d3152e20c`  
		Last Modified: Mon, 18 Nov 2024 15:41:14 GMT  
		Size: 40.4 MB (40351609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8924ec273e919caf7a8a1210fc8992a235b183678e7686dd941b3f295287a`  
		Last Modified: Mon, 18 Nov 2024 15:41:13 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b1adc6ea76ee1a63da85d99c948134d2f3a81ea73d7383aa5e8c3878cc1e5`  
		Last Modified: Mon, 18 Nov 2024 15:41:12 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d34ba125482343643488b81300b7f2ce0aed0c6695145a848c73f0925e5e2`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 1.4 MB (1366618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86e8cffb2db3795823e0a1b7a686bd540c5d02918ef232ca6173d60e2c82c1f`  
		Last Modified: Mon, 18 Nov 2024 15:57:45 GMT  
		Size: 10.9 MB (10890010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff12d6c364e7c870226185011eda5f11ab082357b9d1e1f1fc7083807a1491`  
		Last Modified: Mon, 18 Nov 2024 15:57:49 GMT  
		Size: 101.0 MB (100987987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0da1180f914637f06b82c1be6eaeda13df6c62142bd6bc7c25026bbb9c921f0`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:9e5841ed29ecc752e24909d28f52d776a7cb08c5ea10a5ecdafbf943f4e085cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7b4e806e2e543eb2b07196bd3deca075e913024cb28376da6205288ce17b96`

```dockerfile
```

-	Layers:
	-	`sha256:a930f663b0655f899dc638f1eda5b9af40fda08089b78bc0e5697cf4b1a77277`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 5.4 MB (5427476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce245dd38ad15f6264d37c3569780606360fb353c9f27db162b6229a8c224c0b`  
		Last Modified: Mon, 18 Nov 2024 15:57:44 GMT  
		Size: 29.4 KB (29358 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:a326c789845b43e67fd70ea192992d31dcf818df5fd6767ef7dda74b8223dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180850920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7be82c62dbd13412005728f285f630b21a101f86d5e0c8e37222f0422d35a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD rootfs.tar.xz / # buildkit
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
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV NODE_ENV=production
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 15 Nov 2024 21:19:15 GMT
ENV GHOST_VERSION=5.101.1
# Fri, 15 Nov 2024 21:19:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
WORKDIR /var/lib/ghost
# Fri, 15 Nov 2024 21:19:15 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 15 Nov 2024 21:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 15 Nov 2024 21:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 21:19:15 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 15 Nov 2024 21:19:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5936a9967200e38b9edc3158d32d0bd35fcdadb6ce24041a0fd1a4c31f82bac`  
		Last Modified: Tue, 12 Nov 2024 12:15:56 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34127b12d15850d7834b1077b8c55b769151447e9c26ef585c832e35d5caa0f4`  
		Last Modified: Tue, 12 Nov 2024 17:32:29 GMT  
		Size: 38.4 MB (38403967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682b50f1b1c57d9a4cc8e4b2569ee33bf7d2c5afd57964c5efc69d5bb09df5bb`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 1.7 MB (1708311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068d72d677c3a3b185ce6bb3b5db7e1eb7b1ebd26d8ab52bcff4d7ed2bf6693`  
		Last Modified: Tue, 12 Nov 2024 17:32:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e40c0afde1ff131a4380bd2bb16012712b2bb9b091b56f14888438f693baecc`  
		Last Modified: Wed, 13 Nov 2024 02:22:49 GMT  
		Size: 1.4 MB (1410261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f92cb1aeadc76a8e91374dca4bf3f04465601adbea07f9aa36d57660d4895`  
		Last Modified: Wed, 13 Nov 2024 02:22:50 GMT  
		Size: 10.9 MB (10869645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e6a2863f96037bb86576689a3dd515773e4b3d43e3e4e33ada9ea731e079b2`  
		Last Modified: Sat, 16 Nov 2024 00:10:10 GMT  
		Size: 101.0 MB (100962775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce9224d49b17f4577f5291a40b93f3b124466f532d43090377266a1de80ca62`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:cbd04823c522f5a854665ce8382f3324c65be685bc14e2b857e44a699be89ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131f693be06516c73c7409d0b3f78cf906d14b077cfed59b642f240f8965d7dc`

```dockerfile
```

-	Layers:
	-	`sha256:e4c0e1beb4eddfc2be9cbc018f270692a545b3f1dacd08ad645ed806cacc7699`  
		Last Modified: Sat, 16 Nov 2024 00:10:07 GMT  
		Size: 5.4 MB (5428310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcc27429a3bcb37b1d410f808d89f1e0f11e5f4c2ee74903451f87ec39a059a`  
		Last Modified: Sat, 16 Nov 2024 00:10:06 GMT  
		Size: 29.3 KB (29310 bytes)  
		MIME: application/vnd.in-toto+json

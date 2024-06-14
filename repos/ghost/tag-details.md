<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.85`](#ghost585)
-	[`ghost:5.85-alpine`](#ghost585-alpine)
-	[`ghost:5.85.0`](#ghost5850)
-	[`ghost:5.85.0-alpine`](#ghost5850-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:0b955406619202b5733310209ea3559cddfd6dd18af4dfb3f7f732850e18f784
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
$ docker pull ghost@sha256:82b1a2f8f9278b8fcbaf15e1def87e1f00d4a767baf21054c6b267e6dbaa7265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186327596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c22b5076e36ab51f982706ac9a54188b4433bcdbbfcc8f8fe46bbd44a557b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83321cd735856ec0d7f44f71771e498d1ef57464519f618cc22ad7866ef5947b`  
		Last Modified: Thu, 13 Jun 2024 04:27:07 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25cf008c32b4d657b973595b1f1454769e0f293912451c218d4381aa8cd6fa0`  
		Last Modified: Thu, 13 Jun 2024 04:31:14 GMT  
		Size: 38.2 MB (38182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b8940d2edfd9416327ffd655a668842144f9f2ec6150d134ebbff87abf880e`  
		Last Modified: Thu, 13 Jun 2024 04:31:09 GMT  
		Size: 1.7 MB (1712283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aca9129ef2e2d06f7657678a47c9498bf1905ed7f570190f889ff03acf1b67d`  
		Last Modified: Thu, 13 Jun 2024 04:31:08 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eb2828883da33535df952a1f4b0ba9c48616e0408bef610cb38645b0f03dcc`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 1.4 MB (1447130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b652cfd8ae7279fea1125d7aa75b13f6def55ef5d0e4ec019a529feaf5bf3f`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 11.0 MB (11036480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f22714808a7a9d4aa6964dd32ed1e864d782d4d03558a322a6e67867857941`  
		Last Modified: Thu, 13 Jun 2024 19:13:32 GMT  
		Size: 104.8 MB (104794358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff408453799809622a1d5115da8dc2d97b1f9514b8ad597ff6dce2f598191a`  
		Last Modified: Thu, 13 Jun 2024 19:13:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:4d62fe7e758de64c68de2b8928cbe5213c0a878f2ca8f078f24f35ff796d5a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850d54f9a5210a262d0f47dce96b7d61a7f4db876496fbb21adcacb2c926e8a`

```dockerfile
```

-	Layers:
	-	`sha256:2046accdb92399a3433f7e1dbc71092d3f36574b4192055ffc49d80144bf8cc9`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 4.9 MB (4905678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f643abb810fe0452c1cf6281261c9b14e6894507df1d1078a6399ba07b4e7943`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 29.3 KB (29252 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1709df81f2baaa3caee2c4cc427da1383fdf68d4caae1a93b3e9d4b922a8ce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199093983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65533802d9da43fb48e23c78753d5dfaffe1ec0a352433e9a2c4b853f7ccf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0d7c82e666bdf92b6181a7faa7eecd77a532ad85b50a9e1f79bb1d6613fa9`  
		Last Modified: Thu, 13 Jun 2024 08:25:56 GMT  
		Size: 3.3 KB (3338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c2243e6e8869610976094237f73dc62ecec60f75ea9c64481b52793424440`  
		Last Modified: Thu, 13 Jun 2024 08:29:35 GMT  
		Size: 34.8 MB (34837897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7808f0168b7895c4e99850642982b2557f7fffeaccdc88ecc47ae9ad2981189f`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270dc2a92de47890deeac69d8932fd1a2892b62c1f6677a009a1a04f23d1e2e`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600f4d1f2b28e7188b03405c4c668a87eb6e82fdfab9c345e0446e0e0828f629`  
		Last Modified: Fri, 14 Jun 2024 05:46:11 GMT  
		Size: 1.4 MB (1415609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbc36cd5043fc80940a0a2baf8b5a5a70cd876b754077ad6e5d1c646b957de0`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 11.0 MB (11038122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349135efd0d39d61d87b817398d454885401c78eb3770f777d7da56a2f1e0c28`  
		Last Modified: Fri, 14 Jun 2024 05:46:15 GMT  
		Size: 125.3 MB (125345185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cfdb5ccc7e24d23360175f85bda175dd64cefedc23d7a3a77775b3e357e32`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:8ecd5102ffb242800554e42dd8299c77257b46a1064385c4c1cb513f10ec68a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4c9b79ac39bbd8ae2aa9ef61f4d6987802b0b29c450270f3dedd16b2d9060f`

```dockerfile
```

-	Layers:
	-	`sha256:cf31726accf8f0b17188d5eb844c40357ed972f52a1b49fe4038ad0c3add82bb`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 4.9 MB (4910898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cafaf29a9a1b8bf222e1730c17b5efd7bde5badc5bce919050dadc061d33e6`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d4950c450cdb73d331d4d381f0bb88ef952d3ca62567f6e8f38288450026f7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203944811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573a3bab674697ce84224971f16059f766f88737548d36f300880e5fad0f7a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93232e0688ea9a1bd1b732c9f1b2c9c03b6911315fdae5d8010ef3befa2ab38d`  
		Last Modified: Thu, 13 Jun 2024 02:34:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c00588b3f7973de2ef2c385fbc37567ddf839d8e3526f17ee3ef5e28a764c7`  
		Last Modified: Thu, 13 Jun 2024 02:38:30 GMT  
		Size: 38.2 MB (38231793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2440e46788fef68238f6e632cb588eafaab249ac7bc57b5e11d9f04093c96e`  
		Last Modified: Thu, 13 Jun 2024 02:38:26 GMT  
		Size: 1.7 MB (1712399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17321a6c18adb4ba278dd7daf55fa52f7ab1fbfeec305d6d0088b52805eb3caf`  
		Last Modified: Thu, 13 Jun 2024 02:38:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27f3c57c7979b9ea96fd6ec89febbb7f99d48c217a0cfce5a961c8cb51c7e4e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 1.4 MB (1379703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4500afa4ff9a23e1a1c4f79474e6532ea919adcd46078991ccbf25c5e5a541`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 11.0 MB (11036366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c013b8b9af0d55f2a9fd7284dcc6f5e193b1b89c91d8cbd837ab6a582e70f`  
		Last Modified: Fri, 14 Jun 2024 03:37:52 GMT  
		Size: 122.4 MB (122400522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6892d0cf8cbbf4bb8b053e5a000d3f21cc4f482ee9c59df5806e3c189495fe`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:5a1bfcde450da6835f44d1d7a8cf05313bf7ac37a840f767f78f67dce08a4bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ae29c9bdf31a743e34f863d51d6b9adbe83ca2cb1b96b596fc803f000bd669`

```dockerfile
```

-	Layers:
	-	`sha256:6b1d82e8f5522228955d1a10ca42e25dd03ee7b8530a2f4eccc247536e0dc37e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 4.9 MB (4905928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7c7edad7b5649b9e5402691183648890c02a9f342c61383cac4f5cbbb1da92`  
		Last Modified: Fri, 14 Jun 2024 03:37:48 GMT  
		Size: 29.6 KB (29564 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:5494f59674bdb1b4b66c881eecd9c147ed733de24fb948131d6aac6c08df28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199946720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd5eedfbc4a1deb04953bfddf86c21949e85cd56cffb5ef85a24dea63819c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36295ec3ba3541c3ec5a9cc5bc2bc9cd941c513e8919fc75e7ad60c9663d3040`  
		Last Modified: Thu, 13 Jun 2024 02:30:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ddae058bfede46291d86fb7df520eff1e1a81d1d6a22fbeca96bfb0702a524`  
		Last Modified: Thu, 13 Jun 2024 02:34:22 GMT  
		Size: 40.3 MB (40267253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf5e9391a8b5bac62bb1986c82039e2bb1f31f75ed16b14e63ecbf06cc2ea05`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 1.7 MB (1712580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b803b96e3c7c9f7b9f5aa12159abd1d1ea1325540baa4615991c33e68018ba`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3364820b3f9304e21f1639cd12a1261b9977542860ce64fdf90991281b51775`  
		Last Modified: Fri, 14 Jun 2024 12:02:50 GMT  
		Size: 1.4 MB (1369726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d89e32de6ff3251543a49320164df9abee8c4580d5e1d499e0f84245c861da`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 11.0 MB (11041040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8eabc018f8b7b4d64c1f57ea1f1b25cd5e4afebce49952fc14a380a4e46eb`  
		Last Modified: Fri, 14 Jun 2024 12:02:53 GMT  
		Size: 112.4 MB (112410562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c734c0dfe9e4520dca31e12c901d40a3bd8f644bee482b6301be27359b48`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:4a3de473f22086a370246e1baeb4b257b34798f047d80fa23a4c6ec8a43201a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9443b785470eb378e72ed0cff8a10414948e82028f8b8381e51da03cec356587`

```dockerfile
```

-	Layers:
	-	`sha256:317830f0ec13e18693239aaa663c0cbd10e1194523215fe22840410ff18ae9c6`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 4.9 MB (4903289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4dffa416dcf3cb61dbfe4957154637f4f4597a5c0d308658eaa27a6dcf3c88`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 29.3 KB (29296 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:7af290346132fa2f3e3156be2792426693f67c133394a6765b34c99f67bced74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192492307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a59454af7505b8720c761453d7b706d71cc15ffff50c9f869ebfbafba2065b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ccb6bae7d096f50cba56f9f2aa1f03ee3dd9a7334611148fead591d80eb9f3`  
		Last Modified: Thu, 13 Jun 2024 02:16:12 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f55522c24903fee9511de877b71b62065ca551bb0face860ebdc196cee4e5`  
		Last Modified: Thu, 13 Jun 2024 02:18:00 GMT  
		Size: 38.4 MB (38407320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479cca73a1d0783333ed2a6be245e2ced3268723ca62b5b91424fc51df29f57e`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 1.7 MB (1712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32f3f29401aac472adaf1693462969f69922260c2af6ae418774f082ef8ac0`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff04e017861850e17af5be014e0aee0bf56ce0c7d9f484d9abaf1872806580`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 1.4 MB (1413283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888c67052e34a60cf551ff3d00622d3cebf8eb9fe33ed8e8f7fe5835535e6196`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 11.0 MB (11035540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2191d10dc6cbeebae88389cf306f39408bc4cdaa412fb96982954d5c579ab4c`  
		Last Modified: Fri, 14 Jun 2024 08:17:49 GMT  
		Size: 112.4 MB (112406956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853f87a1f9a7f047a11890981cba11253c16c8c6cace32db3f62023640b4a44`  
		Last Modified: Fri, 14 Jun 2024 08:17:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:f4febeccc2ef4d6425d2f76d4a4ea5443fbaf1ee0ee783a3c32b99582ae57f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5bf875d962e1e717943aac6d3ccae35cbfebbb62ee1e8d1a25e9f1094eead`

```dockerfile
```

-	Layers:
	-	`sha256:5311ed98b2e1064dad9cbe442aded2b68ab152d968a8d17b9345b96219486c22`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 4.9 MB (4898869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7776170a68e0700fcc315e9f064f8292e3c741699971ad934ba6e5abc94b582f`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 29.3 KB (29254 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:c642eb9f06a30c79e4d07783fe962717442d3b1ca84e7be92f552e1138d743fc
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
$ docker pull ghost@sha256:8d073fac5b51f9b55cd465961975ab360a404fd8e7cd6cf5bbdc19c6241834ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158788082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9fff3d74d125be845f565ca35ab3db53cb7e79ace54516e11452fe241657ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 17:53:33 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 17:53:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 17:53:41 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 17:53:47 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 17:53:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 17:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 17:53:47 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1c9f206b0ada39b275ff8cef66cced6071a49a7b91333434265daa1fd21c8`  
		Last Modified: Tue, 04 Jun 2024 17:58:05 GMT  
		Size: 39.8 MB (39832591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b008c3ce085b60d73cf032b1132049496bc297d658e195cb4dc47e73469cce`  
		Last Modified: Tue, 04 Jun 2024 17:57:59 GMT  
		Size: 1.4 MB (1382435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d85c8d7ff2243bd1cb918d46bc1bb98c3f365b4f512ffed8a68ae0a028f243`  
		Last Modified: Tue, 04 Jun 2024 17:58:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c427d56cb4efdc045d19c7f709dc464fc05d1fdaa3643a1ca1e40251a61f5`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c547844624d9e3834f2c0fe47eb0a36916ee360b907d44cd2b601151f3634a`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 776.1 KB (776135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd046384f3bc0ff9aa669bfd4cfde63d1c9177644d924cd059befe3e29ab8ef7`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 11.0 MB (11037085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dd1001786ed403184462aa7e8a9f3299e4ae57c37241d6c4812bce8b64b1a9`  
		Last Modified: Mon, 10 Jun 2024 23:45:40 GMT  
		Size: 102.3 MB (102338928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd4715adfec65ac9fe1fc5d75afe5fc67891ce97ee940f105d62750883ae5f`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9006e8a94d5ee51637c380911df79d8aad5571cb4b30b5718f28d227be8e2f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fed3d6d2d2781f7ba10e9f4179d2de5db6a3fd6b2b58c879eb491bdbbffbf8`

```dockerfile
```

-	Layers:
	-	`sha256:390f9942531a2b8923fcd81867ae59b5f93be3b3b180c64569f29f1bd3827640`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 2.8 MB (2819883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e41e8f2e2f300cefdff332355ddffa24b355864d8546d45f41a701595f94c9f`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 26.6 KB (26575 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:81ae4be92657149131f9b2266f36f09378320a57454b08e7aa27bbc3d7f994c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165427509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc9eba7a2bc8a3e6449c68ef29ccca4de75cd274777e58a6fd26d0cd0a7287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 23:46:28 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 00:26:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 00:26:54 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 00:27:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 00:27:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 00:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 00:27:02 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3dd9d58d81902b90849c04e653ecccebc88fdc5c8fb62407603cf77928f411`  
		Last Modified: Wed, 05 Jun 2024 01:13:56 GMT  
		Size: 38.4 MB (38419934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54cd0ab8460b5de3dd2c93fab4dd58f9ac722bd590887eb1ffa89217760b903`  
		Last Modified: Wed, 05 Jun 2024 01:13:48 GMT  
		Size: 1.4 MB (1382454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f59193cc87af18fc62f2ca5845fa5bcfd61dff1bb8cbcbb223a124b6005df`  
		Last Modified: Wed, 05 Jun 2024 01:13:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049f6f520bd25da7885e9abb9b24fcdabd8151182707156c259762b5326d6b4c`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 11.3 KB (11292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8d160def369bb1b35e14b2efa2d5e6bf33f3f66f74d2c94abc585293fe321`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 768.0 KB (768022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e7f03aedb5c96decdf8693258a43e19b25ef035b92e65cc725f8193b5a302`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 11.0 MB (11046597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa22cf75afe140f3af708bbd9587ac2890ff7770477c2346551029ec8a2980`  
		Last Modified: Mon, 10 Jun 2024 23:57:29 GMT  
		Size: 110.6 MB (110632783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7613c57f53c8ff43758eea5c97a918919281c3ce882fcb18298fea3f798cf`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e1db7f5dc7d70bfb2adcc53f8db9946a02157eff4009dbf5145fe545786eb203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04694ceaa019ec3aeaff8469e5068e7a16467f2e44e7c924c82d13e4befbfaae`

```dockerfile
```

-	Layers:
	-	`sha256:e58cf4ff59b44bb2c763b453d6d94850eed7b32b52d796986b8d006c38f2521f`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 26.5 KB (26465 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4f63a85d9f7c5803d1df82c7b85bf73076aabc47f3915d47a4b17ee3528972bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164300369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf8f342341e3a1eef2f1c5ab5a8f9baa24947a852d53c5b1fd1032e0557c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 01:27:09 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 01:53:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 01:53:53 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 01:53:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 01:53:59 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 01:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 01:53:59 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4da46074b45be618e0aa2b50394ab2dc06c81b838089ee7e34b8c16af82fe9`  
		Last Modified: Wed, 05 Jun 2024 02:20:01 GMT  
		Size: 37.9 MB (37924818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa68cde0fddb2d476f5305613065243911b10a15f602dc4fa43055e2e2c22a39`  
		Last Modified: Wed, 05 Jun 2024 02:19:56 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e55f617bd1628094a3f97e9f9fc5f5c16e858c122a14995aac9b0e804fa0fa9`  
		Last Modified: Wed, 05 Jun 2024 02:19:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbdc20698b92e2ac0817aa82b5aa13db15871e0df14b539cdffe8156699aa2`  
		Last Modified: Wed, 05 Jun 2024 06:02:38 GMT  
		Size: 11.1 KB (11081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82daf8f2b91c9f8f6b17a9ac0b813235d3e8096522da75937710aa480739c78d`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 701.3 KB (701266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44156ed6d22515fc6200afdc32c4b54c9710fdbd36c498bcb6f7354d258d12c`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 11.0 MB (11037716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecefa02e0d55719b20c11d17a7326f7d97ec39221791af6a8a693472c9958a7`  
		Last Modified: Tue, 11 Jun 2024 03:06:16 GMT  
		Size: 110.3 MB (110323116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04d0dcc5d1a6705674092660d91c0a4e9adbc6a76a81242e95b21625834e5c`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:cd7b3062add43adb506e47825afcd5723028c7557e2b1e55212016b924f12d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2839957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80522c31fb61e6b450cf4d7dfc362c21ceec1f63a75761c928ed0a21e987593`

```dockerfile
```

-	Layers:
	-	`sha256:8309d6f000084debdc20f77c23e7f375b8ad6394a115f1208970b3aaca382b64`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 2.8 MB (2813273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b699f696bba3f4d9618e0d81f8252e6c44e29638ce9d5eb9152e612e49fc83`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 26.7 KB (26684 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:84f7e4677c4ed713122b73ac70e6ecebffdf1a5d7fb482ce5a679957b121ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178223389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc4184275a013516f3bbbd9e6740db17dfb5a5aa4e46c1ed2d09528df28d3fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 21:08:08 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 22:27:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 22:27:00 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 22:27:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 22:27:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 22:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 22:27:05 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491f6fd7ddae6df4b5a78beb0a17650e05523856ed7f0a04ac13f587950cc25c`  
		Last Modified: Tue, 04 Jun 2024 22:51:14 GMT  
		Size: 39.5 MB (39535780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020c69bb2a8f95ad36a70c953e64dbf80ce5e5e93938e496b4425a9331e46fd`  
		Last Modified: Tue, 04 Jun 2024 22:51:10 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a439cac09e97e8fb84c14d7262131784dc199dfe117b506a8379ebb5c43a73`  
		Last Modified: Tue, 04 Jun 2024 22:51:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c44f3ffc68d7c0f75ed1c46ecb14c204c42732bc4829e3d5fc6abc9803c747`  
		Last Modified: Wed, 05 Jun 2024 00:18:32 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69088e196f357ee6e1e466846b81d928997f88a2f903e23f0e35306f015f8999`  
		Last Modified: Wed, 05 Jun 2024 00:18:33 GMT  
		Size: 852.9 KB (852858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac7e87a93d1d402fc247b7ed91263b1dfe5244b33a5edfa43f0bff3f51f128`  
		Last Modified: Wed, 05 Jun 2024 00:18:34 GMT  
		Size: 11.0 MB (11036103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438fa7ceedfab1bb9443e0c5abcb0fd487977410ff56460537d951b01ae6862`  
		Last Modified: Tue, 11 Jun 2024 03:32:39 GMT  
		Size: 122.1 MB (122055786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e335dc36adbe12b3f04a94a19f60aba5c5dec4ecbe6e2304a4cf3a41df342f0e`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06f700233fe72f8e2f2ed7d412f99fe27c5a6f4f1d347d1deb8c0782ceef2056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaec7c21bf9dfe7a1d9c9110ebdf3c90c659125afb7a04db8f6076d5c6e186c`

```dockerfile
```

-	Layers:
	-	`sha256:d097b4e149e4b12475304fe7dd57a6bfd56f29b32bd14135ccc8345a7f718892`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 2.8 MB (2819939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecd094df94be85c99c93220c1d50a30af9665a47de25dec75fbca47eeb6ff89`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.85`

```console
$ docker pull ghost@sha256:0b955406619202b5733310209ea3559cddfd6dd18af4dfb3f7f732850e18f784
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

### `ghost:5.85` - linux; amd64

```console
$ docker pull ghost@sha256:82b1a2f8f9278b8fcbaf15e1def87e1f00d4a767baf21054c6b267e6dbaa7265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186327596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c22b5076e36ab51f982706ac9a54188b4433bcdbbfcc8f8fe46bbd44a557b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83321cd735856ec0d7f44f71771e498d1ef57464519f618cc22ad7866ef5947b`  
		Last Modified: Thu, 13 Jun 2024 04:27:07 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25cf008c32b4d657b973595b1f1454769e0f293912451c218d4381aa8cd6fa0`  
		Last Modified: Thu, 13 Jun 2024 04:31:14 GMT  
		Size: 38.2 MB (38182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b8940d2edfd9416327ffd655a668842144f9f2ec6150d134ebbff87abf880e`  
		Last Modified: Thu, 13 Jun 2024 04:31:09 GMT  
		Size: 1.7 MB (1712283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aca9129ef2e2d06f7657678a47c9498bf1905ed7f570190f889ff03acf1b67d`  
		Last Modified: Thu, 13 Jun 2024 04:31:08 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eb2828883da33535df952a1f4b0ba9c48616e0408bef610cb38645b0f03dcc`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 1.4 MB (1447130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b652cfd8ae7279fea1125d7aa75b13f6def55ef5d0e4ec019a529feaf5bf3f`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 11.0 MB (11036480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f22714808a7a9d4aa6964dd32ed1e864d782d4d03558a322a6e67867857941`  
		Last Modified: Thu, 13 Jun 2024 19:13:32 GMT  
		Size: 104.8 MB (104794358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff408453799809622a1d5115da8dc2d97b1f9514b8ad597ff6dce2f598191a`  
		Last Modified: Thu, 13 Jun 2024 19:13:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85` - unknown; unknown

```console
$ docker pull ghost@sha256:4d62fe7e758de64c68de2b8928cbe5213c0a878f2ca8f078f24f35ff796d5a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850d54f9a5210a262d0f47dce96b7d61a7f4db876496fbb21adcacb2c926e8a`

```dockerfile
```

-	Layers:
	-	`sha256:2046accdb92399a3433f7e1dbc71092d3f36574b4192055ffc49d80144bf8cc9`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 4.9 MB (4905678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f643abb810fe0452c1cf6281261c9b14e6894507df1d1078a6399ba07b4e7943`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 29.3 KB (29252 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1709df81f2baaa3caee2c4cc427da1383fdf68d4caae1a93b3e9d4b922a8ce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199093983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65533802d9da43fb48e23c78753d5dfaffe1ec0a352433e9a2c4b853f7ccf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0d7c82e666bdf92b6181a7faa7eecd77a532ad85b50a9e1f79bb1d6613fa9`  
		Last Modified: Thu, 13 Jun 2024 08:25:56 GMT  
		Size: 3.3 KB (3338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c2243e6e8869610976094237f73dc62ecec60f75ea9c64481b52793424440`  
		Last Modified: Thu, 13 Jun 2024 08:29:35 GMT  
		Size: 34.8 MB (34837897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7808f0168b7895c4e99850642982b2557f7fffeaccdc88ecc47ae9ad2981189f`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270dc2a92de47890deeac69d8932fd1a2892b62c1f6677a009a1a04f23d1e2e`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600f4d1f2b28e7188b03405c4c668a87eb6e82fdfab9c345e0446e0e0828f629`  
		Last Modified: Fri, 14 Jun 2024 05:46:11 GMT  
		Size: 1.4 MB (1415609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbc36cd5043fc80940a0a2baf8b5a5a70cd876b754077ad6e5d1c646b957de0`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 11.0 MB (11038122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349135efd0d39d61d87b817398d454885401c78eb3770f777d7da56a2f1e0c28`  
		Last Modified: Fri, 14 Jun 2024 05:46:15 GMT  
		Size: 125.3 MB (125345185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cfdb5ccc7e24d23360175f85bda175dd64cefedc23d7a3a77775b3e357e32`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85` - unknown; unknown

```console
$ docker pull ghost@sha256:8ecd5102ffb242800554e42dd8299c77257b46a1064385c4c1cb513f10ec68a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4c9b79ac39bbd8ae2aa9ef61f4d6987802b0b29c450270f3dedd16b2d9060f`

```dockerfile
```

-	Layers:
	-	`sha256:cf31726accf8f0b17188d5eb844c40357ed972f52a1b49fe4038ad0c3add82bb`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 4.9 MB (4910898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cafaf29a9a1b8bf222e1730c17b5efd7bde5badc5bce919050dadc061d33e6`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d4950c450cdb73d331d4d381f0bb88ef952d3ca62567f6e8f38288450026f7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203944811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573a3bab674697ce84224971f16059f766f88737548d36f300880e5fad0f7a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93232e0688ea9a1bd1b732c9f1b2c9c03b6911315fdae5d8010ef3befa2ab38d`  
		Last Modified: Thu, 13 Jun 2024 02:34:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c00588b3f7973de2ef2c385fbc37567ddf839d8e3526f17ee3ef5e28a764c7`  
		Last Modified: Thu, 13 Jun 2024 02:38:30 GMT  
		Size: 38.2 MB (38231793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2440e46788fef68238f6e632cb588eafaab249ac7bc57b5e11d9f04093c96e`  
		Last Modified: Thu, 13 Jun 2024 02:38:26 GMT  
		Size: 1.7 MB (1712399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17321a6c18adb4ba278dd7daf55fa52f7ab1fbfeec305d6d0088b52805eb3caf`  
		Last Modified: Thu, 13 Jun 2024 02:38:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27f3c57c7979b9ea96fd6ec89febbb7f99d48c217a0cfce5a961c8cb51c7e4e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 1.4 MB (1379703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4500afa4ff9a23e1a1c4f79474e6532ea919adcd46078991ccbf25c5e5a541`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 11.0 MB (11036366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c013b8b9af0d55f2a9fd7284dcc6f5e193b1b89c91d8cbd837ab6a582e70f`  
		Last Modified: Fri, 14 Jun 2024 03:37:52 GMT  
		Size: 122.4 MB (122400522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6892d0cf8cbbf4bb8b053e5a000d3f21cc4f482ee9c59df5806e3c189495fe`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85` - unknown; unknown

```console
$ docker pull ghost@sha256:5a1bfcde450da6835f44d1d7a8cf05313bf7ac37a840f767f78f67dce08a4bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ae29c9bdf31a743e34f863d51d6b9adbe83ca2cb1b96b596fc803f000bd669`

```dockerfile
```

-	Layers:
	-	`sha256:6b1d82e8f5522228955d1a10ca42e25dd03ee7b8530a2f4eccc247536e0dc37e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 4.9 MB (4905928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7c7edad7b5649b9e5402691183648890c02a9f342c61383cac4f5cbbb1da92`  
		Last Modified: Fri, 14 Jun 2024 03:37:48 GMT  
		Size: 29.6 KB (29564 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85` - linux; ppc64le

```console
$ docker pull ghost@sha256:5494f59674bdb1b4b66c881eecd9c147ed733de24fb948131d6aac6c08df28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199946720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd5eedfbc4a1deb04953bfddf86c21949e85cd56cffb5ef85a24dea63819c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36295ec3ba3541c3ec5a9cc5bc2bc9cd941c513e8919fc75e7ad60c9663d3040`  
		Last Modified: Thu, 13 Jun 2024 02:30:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ddae058bfede46291d86fb7df520eff1e1a81d1d6a22fbeca96bfb0702a524`  
		Last Modified: Thu, 13 Jun 2024 02:34:22 GMT  
		Size: 40.3 MB (40267253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf5e9391a8b5bac62bb1986c82039e2bb1f31f75ed16b14e63ecbf06cc2ea05`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 1.7 MB (1712580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b803b96e3c7c9f7b9f5aa12159abd1d1ea1325540baa4615991c33e68018ba`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3364820b3f9304e21f1639cd12a1261b9977542860ce64fdf90991281b51775`  
		Last Modified: Fri, 14 Jun 2024 12:02:50 GMT  
		Size: 1.4 MB (1369726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d89e32de6ff3251543a49320164df9abee8c4580d5e1d499e0f84245c861da`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 11.0 MB (11041040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8eabc018f8b7b4d64c1f57ea1f1b25cd5e4afebce49952fc14a380a4e46eb`  
		Last Modified: Fri, 14 Jun 2024 12:02:53 GMT  
		Size: 112.4 MB (112410562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c734c0dfe9e4520dca31e12c901d40a3bd8f644bee482b6301be27359b48`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85` - unknown; unknown

```console
$ docker pull ghost@sha256:4a3de473f22086a370246e1baeb4b257b34798f047d80fa23a4c6ec8a43201a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9443b785470eb378e72ed0cff8a10414948e82028f8b8381e51da03cec356587`

```dockerfile
```

-	Layers:
	-	`sha256:317830f0ec13e18693239aaa663c0cbd10e1194523215fe22840410ff18ae9c6`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 4.9 MB (4903289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4dffa416dcf3cb61dbfe4957154637f4f4597a5c0d308658eaa27a6dcf3c88`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 29.3 KB (29296 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85` - linux; s390x

```console
$ docker pull ghost@sha256:7af290346132fa2f3e3156be2792426693f67c133394a6765b34c99f67bced74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192492307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a59454af7505b8720c761453d7b706d71cc15ffff50c9f869ebfbafba2065b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ccb6bae7d096f50cba56f9f2aa1f03ee3dd9a7334611148fead591d80eb9f3`  
		Last Modified: Thu, 13 Jun 2024 02:16:12 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f55522c24903fee9511de877b71b62065ca551bb0face860ebdc196cee4e5`  
		Last Modified: Thu, 13 Jun 2024 02:18:00 GMT  
		Size: 38.4 MB (38407320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479cca73a1d0783333ed2a6be245e2ced3268723ca62b5b91424fc51df29f57e`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 1.7 MB (1712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32f3f29401aac472adaf1693462969f69922260c2af6ae418774f082ef8ac0`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff04e017861850e17af5be014e0aee0bf56ce0c7d9f484d9abaf1872806580`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 1.4 MB (1413283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888c67052e34a60cf551ff3d00622d3cebf8eb9fe33ed8e8f7fe5835535e6196`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 11.0 MB (11035540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2191d10dc6cbeebae88389cf306f39408bc4cdaa412fb96982954d5c579ab4c`  
		Last Modified: Fri, 14 Jun 2024 08:17:49 GMT  
		Size: 112.4 MB (112406956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853f87a1f9a7f047a11890981cba11253c16c8c6cace32db3f62023640b4a44`  
		Last Modified: Fri, 14 Jun 2024 08:17:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85` - unknown; unknown

```console
$ docker pull ghost@sha256:f4febeccc2ef4d6425d2f76d4a4ea5443fbaf1ee0ee783a3c32b99582ae57f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5bf875d962e1e717943aac6d3ccae35cbfebbb62ee1e8d1a25e9f1094eead`

```dockerfile
```

-	Layers:
	-	`sha256:5311ed98b2e1064dad9cbe442aded2b68ab152d968a8d17b9345b96219486c22`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 4.9 MB (4898869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7776170a68e0700fcc315e9f064f8292e3c741699971ad934ba6e5abc94b582f`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 29.3 KB (29254 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.85-alpine`

```console
$ docker pull ghost@sha256:c642eb9f06a30c79e4d07783fe962717442d3b1ca84e7be92f552e1138d743fc
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

### `ghost:5.85-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:8d073fac5b51f9b55cd465961975ab360a404fd8e7cd6cf5bbdc19c6241834ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158788082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9fff3d74d125be845f565ca35ab3db53cb7e79ace54516e11452fe241657ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 17:53:33 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 17:53:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 17:53:41 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 17:53:47 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 17:53:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 17:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 17:53:47 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1c9f206b0ada39b275ff8cef66cced6071a49a7b91333434265daa1fd21c8`  
		Last Modified: Tue, 04 Jun 2024 17:58:05 GMT  
		Size: 39.8 MB (39832591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b008c3ce085b60d73cf032b1132049496bc297d658e195cb4dc47e73469cce`  
		Last Modified: Tue, 04 Jun 2024 17:57:59 GMT  
		Size: 1.4 MB (1382435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d85c8d7ff2243bd1cb918d46bc1bb98c3f365b4f512ffed8a68ae0a028f243`  
		Last Modified: Tue, 04 Jun 2024 17:58:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c427d56cb4efdc045d19c7f709dc464fc05d1fdaa3643a1ca1e40251a61f5`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c547844624d9e3834f2c0fe47eb0a36916ee360b907d44cd2b601151f3634a`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 776.1 KB (776135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd046384f3bc0ff9aa669bfd4cfde63d1c9177644d924cd059befe3e29ab8ef7`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 11.0 MB (11037085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dd1001786ed403184462aa7e8a9f3299e4ae57c37241d6c4812bce8b64b1a9`  
		Last Modified: Mon, 10 Jun 2024 23:45:40 GMT  
		Size: 102.3 MB (102338928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd4715adfec65ac9fe1fc5d75afe5fc67891ce97ee940f105d62750883ae5f`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9006e8a94d5ee51637c380911df79d8aad5571cb4b30b5718f28d227be8e2f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fed3d6d2d2781f7ba10e9f4179d2de5db6a3fd6b2b58c879eb491bdbbffbf8`

```dockerfile
```

-	Layers:
	-	`sha256:390f9942531a2b8923fcd81867ae59b5f93be3b3b180c64569f29f1bd3827640`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 2.8 MB (2819883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e41e8f2e2f300cefdff332355ddffa24b355864d8546d45f41a701595f94c9f`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 26.6 KB (26575 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:81ae4be92657149131f9b2266f36f09378320a57454b08e7aa27bbc3d7f994c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165427509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc9eba7a2bc8a3e6449c68ef29ccca4de75cd274777e58a6fd26d0cd0a7287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 23:46:28 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 00:26:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 00:26:54 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 00:27:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 00:27:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 00:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 00:27:02 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3dd9d58d81902b90849c04e653ecccebc88fdc5c8fb62407603cf77928f411`  
		Last Modified: Wed, 05 Jun 2024 01:13:56 GMT  
		Size: 38.4 MB (38419934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54cd0ab8460b5de3dd2c93fab4dd58f9ac722bd590887eb1ffa89217760b903`  
		Last Modified: Wed, 05 Jun 2024 01:13:48 GMT  
		Size: 1.4 MB (1382454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f59193cc87af18fc62f2ca5845fa5bcfd61dff1bb8cbcbb223a124b6005df`  
		Last Modified: Wed, 05 Jun 2024 01:13:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049f6f520bd25da7885e9abb9b24fcdabd8151182707156c259762b5326d6b4c`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 11.3 KB (11292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8d160def369bb1b35e14b2efa2d5e6bf33f3f66f74d2c94abc585293fe321`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 768.0 KB (768022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e7f03aedb5c96decdf8693258a43e19b25ef035b92e65cc725f8193b5a302`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 11.0 MB (11046597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa22cf75afe140f3af708bbd9587ac2890ff7770477c2346551029ec8a2980`  
		Last Modified: Mon, 10 Jun 2024 23:57:29 GMT  
		Size: 110.6 MB (110632783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7613c57f53c8ff43758eea5c97a918919281c3ce882fcb18298fea3f798cf`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e1db7f5dc7d70bfb2adcc53f8db9946a02157eff4009dbf5145fe545786eb203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04694ceaa019ec3aeaff8469e5068e7a16467f2e44e7c924c82d13e4befbfaae`

```dockerfile
```

-	Layers:
	-	`sha256:e58cf4ff59b44bb2c763b453d6d94850eed7b32b52d796986b8d006c38f2521f`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 26.5 KB (26465 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4f63a85d9f7c5803d1df82c7b85bf73076aabc47f3915d47a4b17ee3528972bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164300369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf8f342341e3a1eef2f1c5ab5a8f9baa24947a852d53c5b1fd1032e0557c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 01:27:09 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 01:53:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 01:53:53 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 01:53:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 01:53:59 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 01:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 01:53:59 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4da46074b45be618e0aa2b50394ab2dc06c81b838089ee7e34b8c16af82fe9`  
		Last Modified: Wed, 05 Jun 2024 02:20:01 GMT  
		Size: 37.9 MB (37924818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa68cde0fddb2d476f5305613065243911b10a15f602dc4fa43055e2e2c22a39`  
		Last Modified: Wed, 05 Jun 2024 02:19:56 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e55f617bd1628094a3f97e9f9fc5f5c16e858c122a14995aac9b0e804fa0fa9`  
		Last Modified: Wed, 05 Jun 2024 02:19:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbdc20698b92e2ac0817aa82b5aa13db15871e0df14b539cdffe8156699aa2`  
		Last Modified: Wed, 05 Jun 2024 06:02:38 GMT  
		Size: 11.1 KB (11081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82daf8f2b91c9f8f6b17a9ac0b813235d3e8096522da75937710aa480739c78d`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 701.3 KB (701266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44156ed6d22515fc6200afdc32c4b54c9710fdbd36c498bcb6f7354d258d12c`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 11.0 MB (11037716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecefa02e0d55719b20c11d17a7326f7d97ec39221791af6a8a693472c9958a7`  
		Last Modified: Tue, 11 Jun 2024 03:06:16 GMT  
		Size: 110.3 MB (110323116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04d0dcc5d1a6705674092660d91c0a4e9adbc6a76a81242e95b21625834e5c`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:cd7b3062add43adb506e47825afcd5723028c7557e2b1e55212016b924f12d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2839957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80522c31fb61e6b450cf4d7dfc362c21ceec1f63a75761c928ed0a21e987593`

```dockerfile
```

-	Layers:
	-	`sha256:8309d6f000084debdc20f77c23e7f375b8ad6394a115f1208970b3aaca382b64`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 2.8 MB (2813273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b699f696bba3f4d9618e0d81f8252e6c44e29638ce9d5eb9152e612e49fc83`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 26.7 KB (26684 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:84f7e4677c4ed713122b73ac70e6ecebffdf1a5d7fb482ce5a679957b121ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178223389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc4184275a013516f3bbbd9e6740db17dfb5a5aa4e46c1ed2d09528df28d3fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 21:08:08 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 22:27:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 22:27:00 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 22:27:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 22:27:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 22:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 22:27:05 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491f6fd7ddae6df4b5a78beb0a17650e05523856ed7f0a04ac13f587950cc25c`  
		Last Modified: Tue, 04 Jun 2024 22:51:14 GMT  
		Size: 39.5 MB (39535780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020c69bb2a8f95ad36a70c953e64dbf80ce5e5e93938e496b4425a9331e46fd`  
		Last Modified: Tue, 04 Jun 2024 22:51:10 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a439cac09e97e8fb84c14d7262131784dc199dfe117b506a8379ebb5c43a73`  
		Last Modified: Tue, 04 Jun 2024 22:51:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c44f3ffc68d7c0f75ed1c46ecb14c204c42732bc4829e3d5fc6abc9803c747`  
		Last Modified: Wed, 05 Jun 2024 00:18:32 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69088e196f357ee6e1e466846b81d928997f88a2f903e23f0e35306f015f8999`  
		Last Modified: Wed, 05 Jun 2024 00:18:33 GMT  
		Size: 852.9 KB (852858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac7e87a93d1d402fc247b7ed91263b1dfe5244b33a5edfa43f0bff3f51f128`  
		Last Modified: Wed, 05 Jun 2024 00:18:34 GMT  
		Size: 11.0 MB (11036103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438fa7ceedfab1bb9443e0c5abcb0fd487977410ff56460537d951b01ae6862`  
		Last Modified: Tue, 11 Jun 2024 03:32:39 GMT  
		Size: 122.1 MB (122055786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e335dc36adbe12b3f04a94a19f60aba5c5dec4ecbe6e2304a4cf3a41df342f0e`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06f700233fe72f8e2f2ed7d412f99fe27c5a6f4f1d347d1deb8c0782ceef2056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaec7c21bf9dfe7a1d9c9110ebdf3c90c659125afb7a04db8f6076d5c6e186c`

```dockerfile
```

-	Layers:
	-	`sha256:d097b4e149e4b12475304fe7dd57a6bfd56f29b32bd14135ccc8345a7f718892`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 2.8 MB (2819939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecd094df94be85c99c93220c1d50a30af9665a47de25dec75fbca47eeb6ff89`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.85.0`

```console
$ docker pull ghost@sha256:0b955406619202b5733310209ea3559cddfd6dd18af4dfb3f7f732850e18f784
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

### `ghost:5.85.0` - linux; amd64

```console
$ docker pull ghost@sha256:82b1a2f8f9278b8fcbaf15e1def87e1f00d4a767baf21054c6b267e6dbaa7265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186327596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c22b5076e36ab51f982706ac9a54188b4433bcdbbfcc8f8fe46bbd44a557b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83321cd735856ec0d7f44f71771e498d1ef57464519f618cc22ad7866ef5947b`  
		Last Modified: Thu, 13 Jun 2024 04:27:07 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25cf008c32b4d657b973595b1f1454769e0f293912451c218d4381aa8cd6fa0`  
		Last Modified: Thu, 13 Jun 2024 04:31:14 GMT  
		Size: 38.2 MB (38182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b8940d2edfd9416327ffd655a668842144f9f2ec6150d134ebbff87abf880e`  
		Last Modified: Thu, 13 Jun 2024 04:31:09 GMT  
		Size: 1.7 MB (1712283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aca9129ef2e2d06f7657678a47c9498bf1905ed7f570190f889ff03acf1b67d`  
		Last Modified: Thu, 13 Jun 2024 04:31:08 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eb2828883da33535df952a1f4b0ba9c48616e0408bef610cb38645b0f03dcc`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 1.4 MB (1447130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b652cfd8ae7279fea1125d7aa75b13f6def55ef5d0e4ec019a529feaf5bf3f`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 11.0 MB (11036480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f22714808a7a9d4aa6964dd32ed1e864d782d4d03558a322a6e67867857941`  
		Last Modified: Thu, 13 Jun 2024 19:13:32 GMT  
		Size: 104.8 MB (104794358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff408453799809622a1d5115da8dc2d97b1f9514b8ad597ff6dce2f598191a`  
		Last Modified: Thu, 13 Jun 2024 19:13:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0` - unknown; unknown

```console
$ docker pull ghost@sha256:4d62fe7e758de64c68de2b8928cbe5213c0a878f2ca8f078f24f35ff796d5a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850d54f9a5210a262d0f47dce96b7d61a7f4db876496fbb21adcacb2c926e8a`

```dockerfile
```

-	Layers:
	-	`sha256:2046accdb92399a3433f7e1dbc71092d3f36574b4192055ffc49d80144bf8cc9`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 4.9 MB (4905678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f643abb810fe0452c1cf6281261c9b14e6894507df1d1078a6399ba07b4e7943`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 29.3 KB (29252 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1709df81f2baaa3caee2c4cc427da1383fdf68d4caae1a93b3e9d4b922a8ce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199093983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65533802d9da43fb48e23c78753d5dfaffe1ec0a352433e9a2c4b853f7ccf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0d7c82e666bdf92b6181a7faa7eecd77a532ad85b50a9e1f79bb1d6613fa9`  
		Last Modified: Thu, 13 Jun 2024 08:25:56 GMT  
		Size: 3.3 KB (3338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c2243e6e8869610976094237f73dc62ecec60f75ea9c64481b52793424440`  
		Last Modified: Thu, 13 Jun 2024 08:29:35 GMT  
		Size: 34.8 MB (34837897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7808f0168b7895c4e99850642982b2557f7fffeaccdc88ecc47ae9ad2981189f`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270dc2a92de47890deeac69d8932fd1a2892b62c1f6677a009a1a04f23d1e2e`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600f4d1f2b28e7188b03405c4c668a87eb6e82fdfab9c345e0446e0e0828f629`  
		Last Modified: Fri, 14 Jun 2024 05:46:11 GMT  
		Size: 1.4 MB (1415609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbc36cd5043fc80940a0a2baf8b5a5a70cd876b754077ad6e5d1c646b957de0`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 11.0 MB (11038122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349135efd0d39d61d87b817398d454885401c78eb3770f777d7da56a2f1e0c28`  
		Last Modified: Fri, 14 Jun 2024 05:46:15 GMT  
		Size: 125.3 MB (125345185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cfdb5ccc7e24d23360175f85bda175dd64cefedc23d7a3a77775b3e357e32`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0` - unknown; unknown

```console
$ docker pull ghost@sha256:8ecd5102ffb242800554e42dd8299c77257b46a1064385c4c1cb513f10ec68a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4c9b79ac39bbd8ae2aa9ef61f4d6987802b0b29c450270f3dedd16b2d9060f`

```dockerfile
```

-	Layers:
	-	`sha256:cf31726accf8f0b17188d5eb844c40357ed972f52a1b49fe4038ad0c3add82bb`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 4.9 MB (4910898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cafaf29a9a1b8bf222e1730c17b5efd7bde5badc5bce919050dadc061d33e6`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d4950c450cdb73d331d4d381f0bb88ef952d3ca62567f6e8f38288450026f7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203944811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573a3bab674697ce84224971f16059f766f88737548d36f300880e5fad0f7a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93232e0688ea9a1bd1b732c9f1b2c9c03b6911315fdae5d8010ef3befa2ab38d`  
		Last Modified: Thu, 13 Jun 2024 02:34:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c00588b3f7973de2ef2c385fbc37567ddf839d8e3526f17ee3ef5e28a764c7`  
		Last Modified: Thu, 13 Jun 2024 02:38:30 GMT  
		Size: 38.2 MB (38231793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2440e46788fef68238f6e632cb588eafaab249ac7bc57b5e11d9f04093c96e`  
		Last Modified: Thu, 13 Jun 2024 02:38:26 GMT  
		Size: 1.7 MB (1712399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17321a6c18adb4ba278dd7daf55fa52f7ab1fbfeec305d6d0088b52805eb3caf`  
		Last Modified: Thu, 13 Jun 2024 02:38:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27f3c57c7979b9ea96fd6ec89febbb7f99d48c217a0cfce5a961c8cb51c7e4e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 1.4 MB (1379703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4500afa4ff9a23e1a1c4f79474e6532ea919adcd46078991ccbf25c5e5a541`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 11.0 MB (11036366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c013b8b9af0d55f2a9fd7284dcc6f5e193b1b89c91d8cbd837ab6a582e70f`  
		Last Modified: Fri, 14 Jun 2024 03:37:52 GMT  
		Size: 122.4 MB (122400522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6892d0cf8cbbf4bb8b053e5a000d3f21cc4f482ee9c59df5806e3c189495fe`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0` - unknown; unknown

```console
$ docker pull ghost@sha256:5a1bfcde450da6835f44d1d7a8cf05313bf7ac37a840f767f78f67dce08a4bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ae29c9bdf31a743e34f863d51d6b9adbe83ca2cb1b96b596fc803f000bd669`

```dockerfile
```

-	Layers:
	-	`sha256:6b1d82e8f5522228955d1a10ca42e25dd03ee7b8530a2f4eccc247536e0dc37e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 4.9 MB (4905928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7c7edad7b5649b9e5402691183648890c02a9f342c61383cac4f5cbbb1da92`  
		Last Modified: Fri, 14 Jun 2024 03:37:48 GMT  
		Size: 29.6 KB (29564 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:5494f59674bdb1b4b66c881eecd9c147ed733de24fb948131d6aac6c08df28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199946720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd5eedfbc4a1deb04953bfddf86c21949e85cd56cffb5ef85a24dea63819c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36295ec3ba3541c3ec5a9cc5bc2bc9cd941c513e8919fc75e7ad60c9663d3040`  
		Last Modified: Thu, 13 Jun 2024 02:30:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ddae058bfede46291d86fb7df520eff1e1a81d1d6a22fbeca96bfb0702a524`  
		Last Modified: Thu, 13 Jun 2024 02:34:22 GMT  
		Size: 40.3 MB (40267253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf5e9391a8b5bac62bb1986c82039e2bb1f31f75ed16b14e63ecbf06cc2ea05`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 1.7 MB (1712580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b803b96e3c7c9f7b9f5aa12159abd1d1ea1325540baa4615991c33e68018ba`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3364820b3f9304e21f1639cd12a1261b9977542860ce64fdf90991281b51775`  
		Last Modified: Fri, 14 Jun 2024 12:02:50 GMT  
		Size: 1.4 MB (1369726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d89e32de6ff3251543a49320164df9abee8c4580d5e1d499e0f84245c861da`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 11.0 MB (11041040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8eabc018f8b7b4d64c1f57ea1f1b25cd5e4afebce49952fc14a380a4e46eb`  
		Last Modified: Fri, 14 Jun 2024 12:02:53 GMT  
		Size: 112.4 MB (112410562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c734c0dfe9e4520dca31e12c901d40a3bd8f644bee482b6301be27359b48`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0` - unknown; unknown

```console
$ docker pull ghost@sha256:4a3de473f22086a370246e1baeb4b257b34798f047d80fa23a4c6ec8a43201a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9443b785470eb378e72ed0cff8a10414948e82028f8b8381e51da03cec356587`

```dockerfile
```

-	Layers:
	-	`sha256:317830f0ec13e18693239aaa663c0cbd10e1194523215fe22840410ff18ae9c6`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 4.9 MB (4903289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4dffa416dcf3cb61dbfe4957154637f4f4597a5c0d308658eaa27a6dcf3c88`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 29.3 KB (29296 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0` - linux; s390x

```console
$ docker pull ghost@sha256:7af290346132fa2f3e3156be2792426693f67c133394a6765b34c99f67bced74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192492307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a59454af7505b8720c761453d7b706d71cc15ffff50c9f869ebfbafba2065b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ccb6bae7d096f50cba56f9f2aa1f03ee3dd9a7334611148fead591d80eb9f3`  
		Last Modified: Thu, 13 Jun 2024 02:16:12 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f55522c24903fee9511de877b71b62065ca551bb0face860ebdc196cee4e5`  
		Last Modified: Thu, 13 Jun 2024 02:18:00 GMT  
		Size: 38.4 MB (38407320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479cca73a1d0783333ed2a6be245e2ced3268723ca62b5b91424fc51df29f57e`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 1.7 MB (1712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32f3f29401aac472adaf1693462969f69922260c2af6ae418774f082ef8ac0`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff04e017861850e17af5be014e0aee0bf56ce0c7d9f484d9abaf1872806580`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 1.4 MB (1413283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888c67052e34a60cf551ff3d00622d3cebf8eb9fe33ed8e8f7fe5835535e6196`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 11.0 MB (11035540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2191d10dc6cbeebae88389cf306f39408bc4cdaa412fb96982954d5c579ab4c`  
		Last Modified: Fri, 14 Jun 2024 08:17:49 GMT  
		Size: 112.4 MB (112406956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853f87a1f9a7f047a11890981cba11253c16c8c6cace32db3f62023640b4a44`  
		Last Modified: Fri, 14 Jun 2024 08:17:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0` - unknown; unknown

```console
$ docker pull ghost@sha256:f4febeccc2ef4d6425d2f76d4a4ea5443fbaf1ee0ee783a3c32b99582ae57f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5bf875d962e1e717943aac6d3ccae35cbfebbb62ee1e8d1a25e9f1094eead`

```dockerfile
```

-	Layers:
	-	`sha256:5311ed98b2e1064dad9cbe442aded2b68ab152d968a8d17b9345b96219486c22`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 4.9 MB (4898869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7776170a68e0700fcc315e9f064f8292e3c741699971ad934ba6e5abc94b582f`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 29.3 KB (29254 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.85.0-alpine`

```console
$ docker pull ghost@sha256:c642eb9f06a30c79e4d07783fe962717442d3b1ca84e7be92f552e1138d743fc
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

### `ghost:5.85.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:8d073fac5b51f9b55cd465961975ab360a404fd8e7cd6cf5bbdc19c6241834ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158788082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9fff3d74d125be845f565ca35ab3db53cb7e79ace54516e11452fe241657ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 17:53:33 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 17:53:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 17:53:41 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 17:53:47 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 17:53:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 17:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 17:53:47 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1c9f206b0ada39b275ff8cef66cced6071a49a7b91333434265daa1fd21c8`  
		Last Modified: Tue, 04 Jun 2024 17:58:05 GMT  
		Size: 39.8 MB (39832591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b008c3ce085b60d73cf032b1132049496bc297d658e195cb4dc47e73469cce`  
		Last Modified: Tue, 04 Jun 2024 17:57:59 GMT  
		Size: 1.4 MB (1382435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d85c8d7ff2243bd1cb918d46bc1bb98c3f365b4f512ffed8a68ae0a028f243`  
		Last Modified: Tue, 04 Jun 2024 17:58:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c427d56cb4efdc045d19c7f709dc464fc05d1fdaa3643a1ca1e40251a61f5`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c547844624d9e3834f2c0fe47eb0a36916ee360b907d44cd2b601151f3634a`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 776.1 KB (776135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd046384f3bc0ff9aa669bfd4cfde63d1c9177644d924cd059befe3e29ab8ef7`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 11.0 MB (11037085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dd1001786ed403184462aa7e8a9f3299e4ae57c37241d6c4812bce8b64b1a9`  
		Last Modified: Mon, 10 Jun 2024 23:45:40 GMT  
		Size: 102.3 MB (102338928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd4715adfec65ac9fe1fc5d75afe5fc67891ce97ee940f105d62750883ae5f`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9006e8a94d5ee51637c380911df79d8aad5571cb4b30b5718f28d227be8e2f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fed3d6d2d2781f7ba10e9f4179d2de5db6a3fd6b2b58c879eb491bdbbffbf8`

```dockerfile
```

-	Layers:
	-	`sha256:390f9942531a2b8923fcd81867ae59b5f93be3b3b180c64569f29f1bd3827640`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 2.8 MB (2819883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e41e8f2e2f300cefdff332355ddffa24b355864d8546d45f41a701595f94c9f`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 26.6 KB (26575 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:81ae4be92657149131f9b2266f36f09378320a57454b08e7aa27bbc3d7f994c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165427509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc9eba7a2bc8a3e6449c68ef29ccca4de75cd274777e58a6fd26d0cd0a7287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 23:46:28 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 00:26:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 00:26:54 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 00:27:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 00:27:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 00:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 00:27:02 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3dd9d58d81902b90849c04e653ecccebc88fdc5c8fb62407603cf77928f411`  
		Last Modified: Wed, 05 Jun 2024 01:13:56 GMT  
		Size: 38.4 MB (38419934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54cd0ab8460b5de3dd2c93fab4dd58f9ac722bd590887eb1ffa89217760b903`  
		Last Modified: Wed, 05 Jun 2024 01:13:48 GMT  
		Size: 1.4 MB (1382454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f59193cc87af18fc62f2ca5845fa5bcfd61dff1bb8cbcbb223a124b6005df`  
		Last Modified: Wed, 05 Jun 2024 01:13:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049f6f520bd25da7885e9abb9b24fcdabd8151182707156c259762b5326d6b4c`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 11.3 KB (11292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8d160def369bb1b35e14b2efa2d5e6bf33f3f66f74d2c94abc585293fe321`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 768.0 KB (768022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e7f03aedb5c96decdf8693258a43e19b25ef035b92e65cc725f8193b5a302`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 11.0 MB (11046597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa22cf75afe140f3af708bbd9587ac2890ff7770477c2346551029ec8a2980`  
		Last Modified: Mon, 10 Jun 2024 23:57:29 GMT  
		Size: 110.6 MB (110632783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7613c57f53c8ff43758eea5c97a918919281c3ce882fcb18298fea3f798cf`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e1db7f5dc7d70bfb2adcc53f8db9946a02157eff4009dbf5145fe545786eb203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04694ceaa019ec3aeaff8469e5068e7a16467f2e44e7c924c82d13e4befbfaae`

```dockerfile
```

-	Layers:
	-	`sha256:e58cf4ff59b44bb2c763b453d6d94850eed7b32b52d796986b8d006c38f2521f`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 26.5 KB (26465 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4f63a85d9f7c5803d1df82c7b85bf73076aabc47f3915d47a4b17ee3528972bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164300369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf8f342341e3a1eef2f1c5ab5a8f9baa24947a852d53c5b1fd1032e0557c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 01:27:09 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 01:53:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 01:53:53 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 01:53:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 01:53:59 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 01:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 01:53:59 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4da46074b45be618e0aa2b50394ab2dc06c81b838089ee7e34b8c16af82fe9`  
		Last Modified: Wed, 05 Jun 2024 02:20:01 GMT  
		Size: 37.9 MB (37924818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa68cde0fddb2d476f5305613065243911b10a15f602dc4fa43055e2e2c22a39`  
		Last Modified: Wed, 05 Jun 2024 02:19:56 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e55f617bd1628094a3f97e9f9fc5f5c16e858c122a14995aac9b0e804fa0fa9`  
		Last Modified: Wed, 05 Jun 2024 02:19:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbdc20698b92e2ac0817aa82b5aa13db15871e0df14b539cdffe8156699aa2`  
		Last Modified: Wed, 05 Jun 2024 06:02:38 GMT  
		Size: 11.1 KB (11081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82daf8f2b91c9f8f6b17a9ac0b813235d3e8096522da75937710aa480739c78d`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 701.3 KB (701266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44156ed6d22515fc6200afdc32c4b54c9710fdbd36c498bcb6f7354d258d12c`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 11.0 MB (11037716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecefa02e0d55719b20c11d17a7326f7d97ec39221791af6a8a693472c9958a7`  
		Last Modified: Tue, 11 Jun 2024 03:06:16 GMT  
		Size: 110.3 MB (110323116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04d0dcc5d1a6705674092660d91c0a4e9adbc6a76a81242e95b21625834e5c`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:cd7b3062add43adb506e47825afcd5723028c7557e2b1e55212016b924f12d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2839957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80522c31fb61e6b450cf4d7dfc362c21ceec1f63a75761c928ed0a21e987593`

```dockerfile
```

-	Layers:
	-	`sha256:8309d6f000084debdc20f77c23e7f375b8ad6394a115f1208970b3aaca382b64`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 2.8 MB (2813273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b699f696bba3f4d9618e0d81f8252e6c44e29638ce9d5eb9152e612e49fc83`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 26.7 KB (26684 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.85.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:84f7e4677c4ed713122b73ac70e6ecebffdf1a5d7fb482ce5a679957b121ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178223389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc4184275a013516f3bbbd9e6740db17dfb5a5aa4e46c1ed2d09528df28d3fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 21:08:08 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 22:27:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 22:27:00 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 22:27:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 22:27:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 22:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 22:27:05 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491f6fd7ddae6df4b5a78beb0a17650e05523856ed7f0a04ac13f587950cc25c`  
		Last Modified: Tue, 04 Jun 2024 22:51:14 GMT  
		Size: 39.5 MB (39535780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020c69bb2a8f95ad36a70c953e64dbf80ce5e5e93938e496b4425a9331e46fd`  
		Last Modified: Tue, 04 Jun 2024 22:51:10 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a439cac09e97e8fb84c14d7262131784dc199dfe117b506a8379ebb5c43a73`  
		Last Modified: Tue, 04 Jun 2024 22:51:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c44f3ffc68d7c0f75ed1c46ecb14c204c42732bc4829e3d5fc6abc9803c747`  
		Last Modified: Wed, 05 Jun 2024 00:18:32 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69088e196f357ee6e1e466846b81d928997f88a2f903e23f0e35306f015f8999`  
		Last Modified: Wed, 05 Jun 2024 00:18:33 GMT  
		Size: 852.9 KB (852858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac7e87a93d1d402fc247b7ed91263b1dfe5244b33a5edfa43f0bff3f51f128`  
		Last Modified: Wed, 05 Jun 2024 00:18:34 GMT  
		Size: 11.0 MB (11036103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438fa7ceedfab1bb9443e0c5abcb0fd487977410ff56460537d951b01ae6862`  
		Last Modified: Tue, 11 Jun 2024 03:32:39 GMT  
		Size: 122.1 MB (122055786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e335dc36adbe12b3f04a94a19f60aba5c5dec4ecbe6e2304a4cf3a41df342f0e`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.85.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06f700233fe72f8e2f2ed7d412f99fe27c5a6f4f1d347d1deb8c0782ceef2056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaec7c21bf9dfe7a1d9c9110ebdf3c90c659125afb7a04db8f6076d5c6e186c`

```dockerfile
```

-	Layers:
	-	`sha256:d097b4e149e4b12475304fe7dd57a6bfd56f29b32bd14135ccc8345a7f718892`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 2.8 MB (2819939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecd094df94be85c99c93220c1d50a30af9665a47de25dec75fbca47eeb6ff89`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:c642eb9f06a30c79e4d07783fe962717442d3b1ca84e7be92f552e1138d743fc
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
$ docker pull ghost@sha256:8d073fac5b51f9b55cd465961975ab360a404fd8e7cd6cf5bbdc19c6241834ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158788082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9fff3d74d125be845f565ca35ab3db53cb7e79ace54516e11452fe241657ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 17:53:33 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 17:53:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 17:53:41 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 17:53:47 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 17:53:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 17:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 17:53:47 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1c9f206b0ada39b275ff8cef66cced6071a49a7b91333434265daa1fd21c8`  
		Last Modified: Tue, 04 Jun 2024 17:58:05 GMT  
		Size: 39.8 MB (39832591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b008c3ce085b60d73cf032b1132049496bc297d658e195cb4dc47e73469cce`  
		Last Modified: Tue, 04 Jun 2024 17:57:59 GMT  
		Size: 1.4 MB (1382435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d85c8d7ff2243bd1cb918d46bc1bb98c3f365b4f512ffed8a68ae0a028f243`  
		Last Modified: Tue, 04 Jun 2024 17:58:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c427d56cb4efdc045d19c7f709dc464fc05d1fdaa3643a1ca1e40251a61f5`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c547844624d9e3834f2c0fe47eb0a36916ee360b907d44cd2b601151f3634a`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 776.1 KB (776135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd046384f3bc0ff9aa669bfd4cfde63d1c9177644d924cd059befe3e29ab8ef7`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 11.0 MB (11037085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dd1001786ed403184462aa7e8a9f3299e4ae57c37241d6c4812bce8b64b1a9`  
		Last Modified: Mon, 10 Jun 2024 23:45:40 GMT  
		Size: 102.3 MB (102338928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd4715adfec65ac9fe1fc5d75afe5fc67891ce97ee940f105d62750883ae5f`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9006e8a94d5ee51637c380911df79d8aad5571cb4b30b5718f28d227be8e2f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fed3d6d2d2781f7ba10e9f4179d2de5db6a3fd6b2b58c879eb491bdbbffbf8`

```dockerfile
```

-	Layers:
	-	`sha256:390f9942531a2b8923fcd81867ae59b5f93be3b3b180c64569f29f1bd3827640`  
		Last Modified: Mon, 10 Jun 2024 23:45:37 GMT  
		Size: 2.8 MB (2819883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e41e8f2e2f300cefdff332355ddffa24b355864d8546d45f41a701595f94c9f`  
		Last Modified: Mon, 10 Jun 2024 23:45:36 GMT  
		Size: 26.6 KB (26575 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:81ae4be92657149131f9b2266f36f09378320a57454b08e7aa27bbc3d7f994c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165427509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bc9eba7a2bc8a3e6449c68ef29ccca4de75cd274777e58a6fd26d0cd0a7287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 23:46:28 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 00:26:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 00:26:54 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 00:27:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 00:27:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 00:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 00:27:02 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3dd9d58d81902b90849c04e653ecccebc88fdc5c8fb62407603cf77928f411`  
		Last Modified: Wed, 05 Jun 2024 01:13:56 GMT  
		Size: 38.4 MB (38419934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54cd0ab8460b5de3dd2c93fab4dd58f9ac722bd590887eb1ffa89217760b903`  
		Last Modified: Wed, 05 Jun 2024 01:13:48 GMT  
		Size: 1.4 MB (1382454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f59193cc87af18fc62f2ca5845fa5bcfd61dff1bb8cbcbb223a124b6005df`  
		Last Modified: Wed, 05 Jun 2024 01:13:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049f6f520bd25da7885e9abb9b24fcdabd8151182707156c259762b5326d6b4c`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 11.3 KB (11292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8d160def369bb1b35e14b2efa2d5e6bf33f3f66f74d2c94abc585293fe321`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 768.0 KB (768022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e7f03aedb5c96decdf8693258a43e19b25ef035b92e65cc725f8193b5a302`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 11.0 MB (11046597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa22cf75afe140f3af708bbd9587ac2890ff7770477c2346551029ec8a2980`  
		Last Modified: Mon, 10 Jun 2024 23:57:29 GMT  
		Size: 110.6 MB (110632783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7613c57f53c8ff43758eea5c97a918919281c3ce882fcb18298fea3f798cf`  
		Last Modified: Mon, 10 Jun 2024 23:57:27 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e1db7f5dc7d70bfb2adcc53f8db9946a02157eff4009dbf5145fe545786eb203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04694ceaa019ec3aeaff8469e5068e7a16467f2e44e7c924c82d13e4befbfaae`

```dockerfile
```

-	Layers:
	-	`sha256:e58cf4ff59b44bb2c763b453d6d94850eed7b32b52d796986b8d006c38f2521f`  
		Last Modified: Mon, 10 Jun 2024 23:57:26 GMT  
		Size: 26.5 KB (26465 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4f63a85d9f7c5803d1df82c7b85bf73076aabc47f3915d47a4b17ee3528972bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164300369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf8f342341e3a1eef2f1c5ab5a8f9baa24947a852d53c5b1fd1032e0557c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 01:27:09 GMT
ENV NODE_VERSION=18.20.3
# Wed, 05 Jun 2024 01:53:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 05 Jun 2024 01:53:53 GMT
ENV YARN_VERSION=1.22.19
# Wed, 05 Jun 2024 01:53:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Wed, 05 Jun 2024 01:53:59 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 05 Jun 2024 01:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 01:53:59 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4da46074b45be618e0aa2b50394ab2dc06c81b838089ee7e34b8c16af82fe9`  
		Last Modified: Wed, 05 Jun 2024 02:20:01 GMT  
		Size: 37.9 MB (37924818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa68cde0fddb2d476f5305613065243911b10a15f602dc4fa43055e2e2c22a39`  
		Last Modified: Wed, 05 Jun 2024 02:19:56 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e55f617bd1628094a3f97e9f9fc5f5c16e858c122a14995aac9b0e804fa0fa9`  
		Last Modified: Wed, 05 Jun 2024 02:19:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbdc20698b92e2ac0817aa82b5aa13db15871e0df14b539cdffe8156699aa2`  
		Last Modified: Wed, 05 Jun 2024 06:02:38 GMT  
		Size: 11.1 KB (11081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82daf8f2b91c9f8f6b17a9ac0b813235d3e8096522da75937710aa480739c78d`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 701.3 KB (701266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44156ed6d22515fc6200afdc32c4b54c9710fdbd36c498bcb6f7354d258d12c`  
		Last Modified: Wed, 05 Jun 2024 06:02:40 GMT  
		Size: 11.0 MB (11037716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecefa02e0d55719b20c11d17a7326f7d97ec39221791af6a8a693472c9958a7`  
		Last Modified: Tue, 11 Jun 2024 03:06:16 GMT  
		Size: 110.3 MB (110323116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04d0dcc5d1a6705674092660d91c0a4e9adbc6a76a81242e95b21625834e5c`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:cd7b3062add43adb506e47825afcd5723028c7557e2b1e55212016b924f12d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2839957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80522c31fb61e6b450cf4d7dfc362c21ceec1f63a75761c928ed0a21e987593`

```dockerfile
```

-	Layers:
	-	`sha256:8309d6f000084debdc20f77c23e7f375b8ad6394a115f1208970b3aaca382b64`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 2.8 MB (2813273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b699f696bba3f4d9618e0d81f8252e6c44e29638ce9d5eb9152e612e49fc83`  
		Last Modified: Tue, 11 Jun 2024 03:06:12 GMT  
		Size: 26.7 KB (26684 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:84f7e4677c4ed713122b73ac70e6ecebffdf1a5d7fb482ce5a679957b121ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178223389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc4184275a013516f3bbbd9e6740db17dfb5a5aa4e46c1ed2d09528df28d3fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 21:08:08 GMT
ENV NODE_VERSION=18.20.3
# Tue, 04 Jun 2024 22:27:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Tue, 04 Jun 2024 22:27:00 GMT
ENV YARN_VERSION=1.22.19
# Tue, 04 Jun 2024 22:27:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Tue, 04 Jun 2024 22:27:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 04 Jun 2024 22:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 22:27:05 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491f6fd7ddae6df4b5a78beb0a17650e05523856ed7f0a04ac13f587950cc25c`  
		Last Modified: Tue, 04 Jun 2024 22:51:14 GMT  
		Size: 39.5 MB (39535780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020c69bb2a8f95ad36a70c953e64dbf80ce5e5e93938e496b4425a9331e46fd`  
		Last Modified: Tue, 04 Jun 2024 22:51:10 GMT  
		Size: 1.4 MB (1382445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a439cac09e97e8fb84c14d7262131784dc199dfe117b506a8379ebb5c43a73`  
		Last Modified: Tue, 04 Jun 2024 22:51:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c44f3ffc68d7c0f75ed1c46ecb14c204c42732bc4829e3d5fc6abc9803c747`  
		Last Modified: Wed, 05 Jun 2024 00:18:32 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69088e196f357ee6e1e466846b81d928997f88a2f903e23f0e35306f015f8999`  
		Last Modified: Wed, 05 Jun 2024 00:18:33 GMT  
		Size: 852.9 KB (852858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac7e87a93d1d402fc247b7ed91263b1dfe5244b33a5edfa43f0bff3f51f128`  
		Last Modified: Wed, 05 Jun 2024 00:18:34 GMT  
		Size: 11.0 MB (11036103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438fa7ceedfab1bb9443e0c5abcb0fd487977410ff56460537d951b01ae6862`  
		Last Modified: Tue, 11 Jun 2024 03:32:39 GMT  
		Size: 122.1 MB (122055786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e335dc36adbe12b3f04a94a19f60aba5c5dec4ecbe6e2304a4cf3a41df342f0e`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06f700233fe72f8e2f2ed7d412f99fe27c5a6f4f1d347d1deb8c0782ceef2056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaec7c21bf9dfe7a1d9c9110ebdf3c90c659125afb7a04db8f6076d5c6e186c`

```dockerfile
```

-	Layers:
	-	`sha256:d097b4e149e4b12475304fe7dd57a6bfd56f29b32bd14135ccc8345a7f718892`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 2.8 MB (2819939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecd094df94be85c99c93220c1d50a30af9665a47de25dec75fbca47eeb6ff89`  
		Last Modified: Tue, 11 Jun 2024 03:32:36 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:0b955406619202b5733310209ea3559cddfd6dd18af4dfb3f7f732850e18f784
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
$ docker pull ghost@sha256:82b1a2f8f9278b8fcbaf15e1def87e1f00d4a767baf21054c6b267e6dbaa7265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186327596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c22b5076e36ab51f982706ac9a54188b4433bcdbbfcc8f8fe46bbd44a557b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83321cd735856ec0d7f44f71771e498d1ef57464519f618cc22ad7866ef5947b`  
		Last Modified: Thu, 13 Jun 2024 04:27:07 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25cf008c32b4d657b973595b1f1454769e0f293912451c218d4381aa8cd6fa0`  
		Last Modified: Thu, 13 Jun 2024 04:31:14 GMT  
		Size: 38.2 MB (38182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b8940d2edfd9416327ffd655a668842144f9f2ec6150d134ebbff87abf880e`  
		Last Modified: Thu, 13 Jun 2024 04:31:09 GMT  
		Size: 1.7 MB (1712283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aca9129ef2e2d06f7657678a47c9498bf1905ed7f570190f889ff03acf1b67d`  
		Last Modified: Thu, 13 Jun 2024 04:31:08 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eb2828883da33535df952a1f4b0ba9c48616e0408bef610cb38645b0f03dcc`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 1.4 MB (1447130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b652cfd8ae7279fea1125d7aa75b13f6def55ef5d0e4ec019a529feaf5bf3f`  
		Last Modified: Thu, 13 Jun 2024 19:13:30 GMT  
		Size: 11.0 MB (11036480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f22714808a7a9d4aa6964dd32ed1e864d782d4d03558a322a6e67867857941`  
		Last Modified: Thu, 13 Jun 2024 19:13:32 GMT  
		Size: 104.8 MB (104794358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff408453799809622a1d5115da8dc2d97b1f9514b8ad597ff6dce2f598191a`  
		Last Modified: Thu, 13 Jun 2024 19:13:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:4d62fe7e758de64c68de2b8928cbe5213c0a878f2ca8f078f24f35ff796d5a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850d54f9a5210a262d0f47dce96b7d61a7f4db876496fbb21adcacb2c926e8a`

```dockerfile
```

-	Layers:
	-	`sha256:2046accdb92399a3433f7e1dbc71092d3f36574b4192055ffc49d80144bf8cc9`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 4.9 MB (4905678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f643abb810fe0452c1cf6281261c9b14e6894507df1d1078a6399ba07b4e7943`  
		Last Modified: Thu, 13 Jun 2024 19:13:29 GMT  
		Size: 29.3 KB (29252 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1709df81f2baaa3caee2c4cc427da1383fdf68d4caae1a93b3e9d4b922a8ce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199093983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65533802d9da43fb48e23c78753d5dfaffe1ec0a352433e9a2c4b853f7ccf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0d7c82e666bdf92b6181a7faa7eecd77a532ad85b50a9e1f79bb1d6613fa9`  
		Last Modified: Thu, 13 Jun 2024 08:25:56 GMT  
		Size: 3.3 KB (3338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c2243e6e8869610976094237f73dc62ecec60f75ea9c64481b52793424440`  
		Last Modified: Thu, 13 Jun 2024 08:29:35 GMT  
		Size: 34.8 MB (34837897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7808f0168b7895c4e99850642982b2557f7fffeaccdc88ecc47ae9ad2981189f`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270dc2a92de47890deeac69d8932fd1a2892b62c1f6677a009a1a04f23d1e2e`  
		Last Modified: Thu, 13 Jun 2024 08:29:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600f4d1f2b28e7188b03405c4c668a87eb6e82fdfab9c345e0446e0e0828f629`  
		Last Modified: Fri, 14 Jun 2024 05:46:11 GMT  
		Size: 1.4 MB (1415609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbc36cd5043fc80940a0a2baf8b5a5a70cd876b754077ad6e5d1c646b957de0`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 11.0 MB (11038122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349135efd0d39d61d87b817398d454885401c78eb3770f777d7da56a2f1e0c28`  
		Last Modified: Fri, 14 Jun 2024 05:46:15 GMT  
		Size: 125.3 MB (125345185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cfdb5ccc7e24d23360175f85bda175dd64cefedc23d7a3a77775b3e357e32`  
		Last Modified: Fri, 14 Jun 2024 05:46:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:8ecd5102ffb242800554e42dd8299c77257b46a1064385c4c1cb513f10ec68a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4c9b79ac39bbd8ae2aa9ef61f4d6987802b0b29c450270f3dedd16b2d9060f`

```dockerfile
```

-	Layers:
	-	`sha256:cf31726accf8f0b17188d5eb844c40357ed972f52a1b49fe4038ad0c3add82bb`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 4.9 MB (4910898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cafaf29a9a1b8bf222e1730c17b5efd7bde5badc5bce919050dadc061d33e6`  
		Last Modified: Fri, 14 Jun 2024 05:46:10 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d4950c450cdb73d331d4d381f0bb88ef952d3ca62567f6e8f38288450026f7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203944811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573a3bab674697ce84224971f16059f766f88737548d36f300880e5fad0f7a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93232e0688ea9a1bd1b732c9f1b2c9c03b6911315fdae5d8010ef3befa2ab38d`  
		Last Modified: Thu, 13 Jun 2024 02:34:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c00588b3f7973de2ef2c385fbc37567ddf839d8e3526f17ee3ef5e28a764c7`  
		Last Modified: Thu, 13 Jun 2024 02:38:30 GMT  
		Size: 38.2 MB (38231793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2440e46788fef68238f6e632cb588eafaab249ac7bc57b5e11d9f04093c96e`  
		Last Modified: Thu, 13 Jun 2024 02:38:26 GMT  
		Size: 1.7 MB (1712399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17321a6c18adb4ba278dd7daf55fa52f7ab1fbfeec305d6d0088b52805eb3caf`  
		Last Modified: Thu, 13 Jun 2024 02:38:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27f3c57c7979b9ea96fd6ec89febbb7f99d48c217a0cfce5a961c8cb51c7e4e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 1.4 MB (1379703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4500afa4ff9a23e1a1c4f79474e6532ea919adcd46078991ccbf25c5e5a541`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 11.0 MB (11036366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c013b8b9af0d55f2a9fd7284dcc6f5e193b1b89c91d8cbd837ab6a582e70f`  
		Last Modified: Fri, 14 Jun 2024 03:37:52 GMT  
		Size: 122.4 MB (122400522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6892d0cf8cbbf4bb8b053e5a000d3f21cc4f482ee9c59df5806e3c189495fe`  
		Last Modified: Fri, 14 Jun 2024 03:37:50 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:5a1bfcde450da6835f44d1d7a8cf05313bf7ac37a840f767f78f67dce08a4bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ae29c9bdf31a743e34f863d51d6b9adbe83ca2cb1b96b596fc803f000bd669`

```dockerfile
```

-	Layers:
	-	`sha256:6b1d82e8f5522228955d1a10ca42e25dd03ee7b8530a2f4eccc247536e0dc37e`  
		Last Modified: Fri, 14 Jun 2024 03:37:49 GMT  
		Size: 4.9 MB (4905928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7c7edad7b5649b9e5402691183648890c02a9f342c61383cac4f5cbbb1da92`  
		Last Modified: Fri, 14 Jun 2024 03:37:48 GMT  
		Size: 29.6 KB (29564 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:5494f59674bdb1b4b66c881eecd9c147ed733de24fb948131d6aac6c08df28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199946720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd5eedfbc4a1deb04953bfddf86c21949e85cd56cffb5ef85a24dea63819c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36295ec3ba3541c3ec5a9cc5bc2bc9cd941c513e8919fc75e7ad60c9663d3040`  
		Last Modified: Thu, 13 Jun 2024 02:30:40 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ddae058bfede46291d86fb7df520eff1e1a81d1d6a22fbeca96bfb0702a524`  
		Last Modified: Thu, 13 Jun 2024 02:34:22 GMT  
		Size: 40.3 MB (40267253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf5e9391a8b5bac62bb1986c82039e2bb1f31f75ed16b14e63ecbf06cc2ea05`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 1.7 MB (1712580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b803b96e3c7c9f7b9f5aa12159abd1d1ea1325540baa4615991c33e68018ba`  
		Last Modified: Thu, 13 Jun 2024 02:34:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3364820b3f9304e21f1639cd12a1261b9977542860ce64fdf90991281b51775`  
		Last Modified: Fri, 14 Jun 2024 12:02:50 GMT  
		Size: 1.4 MB (1369726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d89e32de6ff3251543a49320164df9abee8c4580d5e1d499e0f84245c861da`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 11.0 MB (11041040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8eabc018f8b7b4d64c1f57ea1f1b25cd5e4afebce49952fc14a380a4e46eb`  
		Last Modified: Fri, 14 Jun 2024 12:02:53 GMT  
		Size: 112.4 MB (112410562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c734c0dfe9e4520dca31e12c901d40a3bd8f644bee482b6301be27359b48`  
		Last Modified: Fri, 14 Jun 2024 12:02:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:4a3de473f22086a370246e1baeb4b257b34798f047d80fa23a4c6ec8a43201a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9443b785470eb378e72ed0cff8a10414948e82028f8b8381e51da03cec356587`

```dockerfile
```

-	Layers:
	-	`sha256:317830f0ec13e18693239aaa663c0cbd10e1194523215fe22840410ff18ae9c6`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 4.9 MB (4903289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4dffa416dcf3cb61dbfe4957154637f4f4597a5c0d308658eaa27a6dcf3c88`  
		Last Modified: Fri, 14 Jun 2024 12:02:49 GMT  
		Size: 29.3 KB (29296 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:7af290346132fa2f3e3156be2792426693f67c133394a6765b34c99f67bced74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192492307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a59454af7505b8720c761453d7b706d71cc15ffff50c9f869ebfbafba2065b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 10 Jun 2024 18:51:12 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 18:51:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_VERSION=18.20.3
# Mon, 10 Jun 2024 18:51:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 10 Jun 2024 18:51:12 GMT
ENV YARN_VERSION=1.22.19
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/*
# Mon, 10 Jun 2024 18:51:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node"]
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GOSU_VERSION=1.16
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV NODE_ENV=production
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CLI_VERSION=1.26.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 10 Jun 2024 18:51:12 GMT
ENV GHOST_VERSION=5.85.0
# Mon, 10 Jun 2024 18:51:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
WORKDIR /var/lib/ghost
# Mon, 10 Jun 2024 18:51:12 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 10 Jun 2024 18:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 10 Jun 2024 18:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 18:51:12 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 10 Jun 2024 18:51:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ccb6bae7d096f50cba56f9f2aa1f03ee3dd9a7334611148fead591d80eb9f3`  
		Last Modified: Thu, 13 Jun 2024 02:16:12 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f55522c24903fee9511de877b71b62065ca551bb0face860ebdc196cee4e5`  
		Last Modified: Thu, 13 Jun 2024 02:18:00 GMT  
		Size: 38.4 MB (38407320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479cca73a1d0783333ed2a6be245e2ced3268723ca62b5b91424fc51df29f57e`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 1.7 MB (1712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32f3f29401aac472adaf1693462969f69922260c2af6ae418774f082ef8ac0`  
		Last Modified: Thu, 13 Jun 2024 02:17:55 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff04e017861850e17af5be014e0aee0bf56ce0c7d9f484d9abaf1872806580`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 1.4 MB (1413283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888c67052e34a60cf551ff3d00622d3cebf8eb9fe33ed8e8f7fe5835535e6196`  
		Last Modified: Fri, 14 Jun 2024 08:17:47 GMT  
		Size: 11.0 MB (11035540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2191d10dc6cbeebae88389cf306f39408bc4cdaa412fb96982954d5c579ab4c`  
		Last Modified: Fri, 14 Jun 2024 08:17:49 GMT  
		Size: 112.4 MB (112406956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853f87a1f9a7f047a11890981cba11253c16c8c6cace32db3f62023640b4a44`  
		Last Modified: Fri, 14 Jun 2024 08:17:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:f4febeccc2ef4d6425d2f76d4a4ea5443fbaf1ee0ee783a3c32b99582ae57f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5bf875d962e1e717943aac6d3ccae35cbfebbb62ee1e8d1a25e9f1094eead`

```dockerfile
```

-	Layers:
	-	`sha256:5311ed98b2e1064dad9cbe442aded2b68ab152d968a8d17b9345b96219486c22`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 4.9 MB (4898869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7776170a68e0700fcc315e9f064f8292e3c741699971ad934ba6e5abc94b582f`  
		Last Modified: Fri, 14 Jun 2024 08:17:46 GMT  
		Size: 29.3 KB (29254 bytes)  
		MIME: application/vnd.in-toto+json

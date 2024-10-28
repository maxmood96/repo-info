<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.98`](#ghost598)
-	[`ghost:5.98-alpine`](#ghost598-alpine)
-	[`ghost:5.98.0`](#ghost5980)
-	[`ghost:5.98.0-alpine`](#ghost5980-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:37ed6c5f04ab1f0a93530b0dcb5a67a51985658f5941ed48fd69bc34d095a913
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
$ docker pull ghost@sha256:0dfea0340260b0bd3ab6de9a7ad399354899f15d9094b9876facc9f6db2755c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174389863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2505b202ad617a1a259f58e421d69e27c4aefaf6036ddbefee53086e6e0ce3d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36857b98621538ae167fc7e123b6fbeedf251abdf778478eaafe6b05832a29`  
		Last Modified: Thu, 17 Oct 2024 01:14:57 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f8c01c1aae756e37730cff35bd7a8397fdaef2891453596ec4fcb0ee04889b`  
		Last Modified: Thu, 17 Oct 2024 01:14:59 GMT  
		Size: 38.2 MB (38179242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3743e02f6e58d326658fb0c27c5211771e74e968dcbf3b8910a3ad6d6065d4c2`  
		Last Modified: Thu, 17 Oct 2024 01:14:57 GMT  
		Size: 1.7 MB (1708106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e8df9e7da85da17a9fc901fbe70e87ce70e9fe842e8dec211bf760448c518`  
		Last Modified: Thu, 17 Oct 2024 01:14:57 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b48401b588e559714a91a0632af8ba1aa9aadc8c84f93e4f3dc77d5f3f2e687`  
		Last Modified: Thu, 24 Oct 2024 22:58:08 GMT  
		Size: 1.4 MB (1444792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefc1693b4627148753751ded8ab16334caf86fe31656ddb4f9f07c2169c5a79`  
		Last Modified: Thu, 24 Oct 2024 22:58:08 GMT  
		Size: 10.9 MB (10865564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecfd7cfd3cfc918339635f56155c8addad60b3f30b78d9456a769d418a4fc7a`  
		Last Modified: Thu, 24 Oct 2024 22:58:09 GMT  
		Size: 93.1 MB (93061538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88015d884e1ea213e78f0cd0d18cfa6ec161322d643e98b97c8897e9eb89c6f`  
		Last Modified: Thu, 24 Oct 2024 22:58:07 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:bb4538f301bb3801bf029d06304a47d46ba1884ee775d8f81181f56283726b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a4c163bcd7e433f9548059410efd90f70b92664f4e70022a588e935769127a`

```dockerfile
```

-	Layers:
	-	`sha256:82a48b82f7f01c63bf7b5ac516fd45a7fd79876051f56ca690c44f5a974691b7`  
		Last Modified: Thu, 24 Oct 2024 22:58:07 GMT  
		Size: 5.4 MB (5420480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1f8a3c2b3124342ab1c38e55303f8ebd480222ee9a32ddcd614eb3770a77e7`  
		Last Modified: Thu, 24 Oct 2024 22:58:07 GMT  
		Size: 29.3 KB (29298 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8944e49ed2420db16af0bfd8044e0dd10791bbcbdaae063084b19fd64d0b98f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186914156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c7f8e097018230bf17c028fca14d798e1d45175a4fd00c9098633d012696d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c93bbfde48f5ab1bafbc7b40d95744dcda2249924d3bff15592f62991d91da`  
		Last Modified: Thu, 17 Oct 2024 14:29:28 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebe513cb685f99655a60ea2a5b1b0f3d9edb1eb05e647f12292cda6b2eba71`  
		Last Modified: Thu, 17 Oct 2024 14:44:08 GMT  
		Size: 34.8 MB (34834252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127a2d4461f22aa32723eebec9d751bada234cb9a3b16deb67991a87430d60e`  
		Last Modified: Thu, 17 Oct 2024 14:44:05 GMT  
		Size: 1.7 MB (1708447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e271a95e4ef89afbc4cfc2550ed87c190f21dce805b9fcf48c71b32939e44`  
		Last Modified: Thu, 17 Oct 2024 14:44:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a098602bac59119360ccade9f82e8cd50b545a24be30c0052fcefba78be607c2`  
		Last Modified: Fri, 18 Oct 2024 06:22:08 GMT  
		Size: 1.4 MB (1412473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd59287296a8abec277b55ab1ba1ba2c171de1880edadd5c71391c57f91e4e06`  
		Last Modified: Fri, 18 Oct 2024 06:22:08 GMT  
		Size: 10.9 MB (10865110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac490d1c26231444b96c3fe5df695c3771a7b8ea48e6fd5a846adf6e19946cda`  
		Last Modified: Thu, 24 Oct 2024 23:03:53 GMT  
		Size: 113.4 MB (113371348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e32200398d5cd0e9d805800c70a8a399e92f519debc1dfd46e58ff7ed33df1`  
		Last Modified: Thu, 24 Oct 2024 23:03:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:253995da89b748b007b7fca0afcd6da38a16327ae94546bd13823d91a5c52bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afd555d84539fe6bb85d63ab13490c90585bf466cf95e3a1806aa718a79ceaa`

```dockerfile
```

-	Layers:
	-	`sha256:fc3e104d5739490d4aa7eff43ed5cf8197d3306e8e7278d683919afd1ee773ba`  
		Last Modified: Thu, 24 Oct 2024 23:03:50 GMT  
		Size: 5.4 MB (5425949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2ffb7e6a00428970b70a2cf1df9c7cdfcd2403a64b8d65ee48f696eb53869b`  
		Last Modified: Thu, 24 Oct 2024 23:03:49 GMT  
		Size: 29.4 KB (29439 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:376624c3083268d6663cadaf896ae31e8ec628ff606d731add0a64e2354d449b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175358055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0ec6080215207ff2ff8a8cc8d7c96f79fea8d4d11ce0c46c0ebfe6c2c672b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ddb100d04a9a60ec43dd82c5f230e3f9a986af5a5d8b341cd2cb860f40c234`  
		Last Modified: Thu, 17 Oct 2024 13:36:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aef2c99b54eb40aaa69ff9b9ab139f0b510eff128f96b45b5beba014e9179a6`  
		Last Modified: Thu, 17 Oct 2024 13:49:16 GMT  
		Size: 38.2 MB (38223612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12af688d404f37010b8656e1ea189016adb20cae63fb49a4c34772f6e5f38882`  
		Last Modified: Thu, 17 Oct 2024 13:49:15 GMT  
		Size: 1.7 MB (1708292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d4419d49088625b08316adca0cb23bf97ca22872cec9c87189f1600ca8ca1d`  
		Last Modified: Thu, 17 Oct 2024 13:49:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656f7a269cf68f35ceeacf03cef909ee99440e93db9cb2fff5ac271598712df2`  
		Last Modified: Wed, 23 Oct 2024 00:11:25 GMT  
		Size: 1.4 MB (1376608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837843f7e3692a14b5c7e4491946f45ef5ebc099963dbf660dddf277b6cf129`  
		Last Modified: Wed, 23 Oct 2024 00:11:25 GMT  
		Size: 10.9 MB (10865809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9749d1d8f1a5d9af077eb35a9531d4c2e82d9731823a536b090b34de8bbe151`  
		Last Modified: Thu, 24 Oct 2024 22:57:02 GMT  
		Size: 94.0 MB (94023061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0dbe29cf7dfa8a68d363c1c08975fd255d17fe10a6c1ff0d08544d6d2c721`  
		Last Modified: Thu, 24 Oct 2024 22:56:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:8bfe9cd0f183dc8491fde9a512bdce10ac7db3059fcf4a208ca6431817cf8c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df33892c27fd824696f1de00498987e92d5b365873b766669c009c799b32571`

```dockerfile
```

-	Layers:
	-	`sha256:b9cacb90a05f7bafa38d23ddde663b0b42f68f962db9e22bdc83c09802d4d932`  
		Last Modified: Thu, 24 Oct 2024 22:57:00 GMT  
		Size: 5.4 MB (5420730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2617a8281cdedd6f06d416a62f3289ac6cc313d3e8ccd10647ade2243603d813`  
		Last Modified: Thu, 24 Oct 2024 22:56:59 GMT  
		Size: 29.5 KB (29468 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:b3f7dc92b242b2735af2326e5bfff5d9fb9e01f52591db50d71ebfbfbef22fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187931874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc15a39d015027190addf9ce0199834ad98dccd76d59029769e3033a2df631c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604818cf87f319cda069f9971e4eae9d29c0ae287449aa7f1402ffbf6fa34b37`  
		Last Modified: Thu, 17 Oct 2024 09:04:40 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37107ff641a94a678b22533233149d3284797c9f9965b6d5c5ec09ef1365432b`  
		Last Modified: Thu, 17 Oct 2024 09:14:52 GMT  
		Size: 40.3 MB (40263098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e51b720c48366d32b3e802e652d96f66446ec9c28bafe6d71b3e8266ad240c5`  
		Last Modified: Thu, 17 Oct 2024 09:14:51 GMT  
		Size: 1.7 MB (1708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a14799ac36d29c01aa65fbbdf2b86861553d005f04ee7d3f16b9a96385d01b`  
		Last Modified: Thu, 17 Oct 2024 09:14:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b653865e0124e1fe5807478369409216fb1c30fcfcae6f5778a0e413e4b1ab2c`  
		Last Modified: Wed, 23 Oct 2024 00:15:26 GMT  
		Size: 1.4 MB (1366548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49d5ff0c0b6859c18d854ac99ea20a0a27944076b84d87c5f987df9e11a02fc`  
		Last Modified: Wed, 23 Oct 2024 00:15:27 GMT  
		Size: 10.9 MB (10867095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ee32d15cd2ca283a5cfce8a4d073a147d5bdc897032df05fff66a85254a09b`  
		Last Modified: Thu, 24 Oct 2024 23:04:38 GMT  
		Size: 100.6 MB (100600271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa470a6fbea78a5b4f609a06f5c959638ade1430e2ceca757aab9385fc854b88`  
		Last Modified: Thu, 24 Oct 2024 23:04:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:289f0dcef973921469dc055ff16ea252705e5165e03d5e692c875f6cba59414a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf4280c5c3b8b588bf54be5b225967c1d0f1f476b7c87381617f8f02f380e2f`

```dockerfile
```

-	Layers:
	-	`sha256:717607b4c7f872a4922459ea715043ad51f40c160d7c3bd6d46634920e84757d`  
		Last Modified: Thu, 24 Oct 2024 23:04:35 GMT  
		Size: 5.4 MB (5416740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9af13cfc3f278bc713db187bfc88b652887e951e3f930309917aabf96957b61`  
		Last Modified: Thu, 24 Oct 2024 23:04:34 GMT  
		Size: 29.4 KB (29385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:3847c55dffb24323a48b5848b12f5178e742e1d5185598a83d7d1d299512f5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180443392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622970d8373ee1f9ebc8290d25c816cb44026dd12736daf61338fd105a88c771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9ccece114e5fd859788dca76e16273103e184aa5fded780b86d30f19feb07`  
		Last Modified: Thu, 17 Oct 2024 13:35:57 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988b585ca6b4a41eed6fc8de77520540958c4b357a1f90351d3025551d6232f8`  
		Last Modified: Thu, 17 Oct 2024 13:44:25 GMT  
		Size: 38.4 MB (38403852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7b5d7017150bc91aced99fb06b326881a9ce6a26f427cfc99ef3db2b0b0f2f`  
		Last Modified: Thu, 17 Oct 2024 13:44:22 GMT  
		Size: 1.7 MB (1708161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9f0c486693be660b5ec37260553c31acb00d8d4fda7289f034ee42cb777fc`  
		Last Modified: Thu, 17 Oct 2024 13:44:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7b3bd1710880e24c4eb7081acea7ff8099ae79aecdb2db33650fccb4d18555`  
		Last Modified: Thu, 17 Oct 2024 19:45:54 GMT  
		Size: 1.4 MB (1410060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a9a3a17c12ba6c739052563b18f443c49d0572fdca0ca4e8144ceccb7f81`  
		Last Modified: Wed, 23 Oct 2024 00:34:43 GMT  
		Size: 10.9 MB (10875398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc455ca987b5a1523f6992875be0655c0d875fe6efea915f4f2a8c2372b147`  
		Last Modified: Thu, 24 Oct 2024 23:12:29 GMT  
		Size: 100.6 MB (100551507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6617aa0598cc9ac91ba5eedee30c1f5da93948aa53b9a5587468d235dc3de8d0`  
		Last Modified: Thu, 24 Oct 2024 23:12:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:937f8bea2c63ccab0c1f70b53da29597573952dd46f127b13d5d241e2dbaa8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7385aca39d77f4f77fb66ae4ebc7a49c374f7ea9dd85c2920a7e2552b2db0284`

```dockerfile
```

-	Layers:
	-	`sha256:fdd65679fca91d9224c84d768eccf9b13434fc5c9cb8bff3e9589512ddf9cd35`  
		Last Modified: Thu, 24 Oct 2024 23:12:27 GMT  
		Size: 5.4 MB (5412214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d4b6fb293aa2b5000d13fd0be052891172e01028ae1e5145d04bb0e36eb4c1`  
		Last Modified: Thu, 24 Oct 2024 23:12:27 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:0fb8d3976ee222fb705bd2de4b8e89946f7fa57e60e54163585c69d8c284ae19
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
$ docker pull ghost@sha256:399e925722b29cb4c9e0e96883da3055f8efb02b997e8020e60841da973adf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147612244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1e74b076553228bee1d1bb15eeafa68223a3c417b4aeba3087ce087a5e5b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5fa6889f28fd528156e3fe0e0a254be528df1dad2e1d2d0ab8cf11131a073d`  
		Last Modified: Fri, 06 Sep 2024 23:16:09 GMT  
		Size: 39.8 MB (39831152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a466315fb2612e923981687f8b8ceb89aa3831ce5224fd75351306a06c7a250`  
		Last Modified: Fri, 06 Sep 2024 23:16:04 GMT  
		Size: 1.4 MB (1382233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ceedeff43cf732f04ee25de7c5bd5c6e18ca1101e2cb89d3ec52e8a15731d2f`  
		Last Modified: Fri, 06 Sep 2024 23:16:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc878b6f56a450ba8fd393fe47b16a0915df0462f52af02dd131d6dca55f4a`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 776.0 KB (776015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55299a314d60873e29861cf074df16d0fa3d47b897f3b83a0ac103bd0ed32032`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 1.1 MB (1121670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f725d1039d87b072201e21cd2519dd7490309443f913e342669f52741059072`  
		Last Modified: Thu, 24 Oct 2024 22:57:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ab5c7f9549dadaa682048914f93f28a03d1acbec11055b61345575fff0ac4a`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 10.9 MB (10864602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a822ca004dd5fb2dbb250ad9368cf08207ee68e760bda86c19c0fed8b1deb8d`  
		Last Modified: Thu, 24 Oct 2024 22:58:00 GMT  
		Size: 90.2 MB (90215669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a8af326984964ef5659f84f11853823064140f03eae9615a1cefbb78ff9c25`  
		Last Modified: Thu, 24 Oct 2024 22:57:58 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b501ed704a68db7178e832c22462c4742c0187cbb6d2b164bd2d5130db181ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0345b1805ef4153a584b18cd74ea179b105dd0a3ce4c8c090b95e410a557b5`

```dockerfile
```

-	Layers:
	-	`sha256:cde9825d30052cc0fee8944e7b4d1e5890644db51d1e76e0820b84695681c553`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 3.3 MB (3311299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd273a0f55ab0441b427a71bf5a888d2408ba0c67099458fbe3b032cad3f49d`  
		Last Modified: Thu, 24 Oct 2024 22:57:56 GMT  
		Size: 32.2 KB (32241 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:fa36d7694df570f7380ec4b4ed6b26b6c1b664046b5bcfca3a74290fe4f8575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154365221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb1fa36b282be069b39c1a7871c000779ffe5494b0e12bf72be49445b149f93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b1ff41b89689262f8588b245bb78190b8a0c16c16c9daf3cebb351bccfdb3`  
		Last Modified: Sat, 07 Sep 2024 07:52:14 GMT  
		Size: 38.4 MB (38420067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4959454224b256e3ad89e9e437a96ca021ed6f390eb5ad33a272adafbb2857e`  
		Last Modified: Sat, 07 Sep 2024 07:52:13 GMT  
		Size: 1.4 MB (1382249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f02e22fa6268f811fb76b6926a490d125499f220d5a7385ac2399517457f49`  
		Last Modified: Sat, 07 Sep 2024 07:52:12 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40680b97610532f1ca37d28c11bfaf7cb9abf82f7f7c24d7f700804314586c72`  
		Last Modified: Sat, 07 Sep 2024 13:37:46 GMT  
		Size: 767.8 KB (767845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7725ea60a425a96c96318772b1bf05da646a7064d297afa87dbc8f58ba5881e3`  
		Last Modified: Sat, 07 Sep 2024 13:37:46 GMT  
		Size: 1.1 MB (1088933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a28d0e08d8b5b681d01d146e049dd8b78d5ad3e2837d766e18f8910c77476`  
		Last Modified: Sat, 07 Sep 2024 13:37:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bf6e85286324b654be61b09098a1042e8f209a879bf1c64e4ddb451049e26b`  
		Last Modified: Sat, 07 Sep 2024 13:37:47 GMT  
		Size: 10.9 MB (10867259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b006d9ed2ae6cc2ca4f2ee6f765c91912fca4a97dbaceec4c7d67197ee919c`  
		Last Modified: Thu, 24 Oct 2024 23:08:22 GMT  
		Size: 98.7 MB (98661284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e95102f31da07ffe64952e7daf107b1f7fa499ffb4937d90c3eefa07a3a0fd6`  
		Last Modified: Thu, 24 Oct 2024 23:08:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:aeb42af488cdf5ca7b05e762ad6dfa7216f8efee5db8228d39bd3dfb09b5d218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3925360d54a904664af63d18bedf6424bb5e8498b60519020ebf4c6ceafa1fd5`

```dockerfile
```

-	Layers:
	-	`sha256:7db64ace60f845e77717a973846d3ab1c297ce6d1b0d588e4ae92a69263b3736`  
		Last Modified: Thu, 24 Oct 2024 23:08:19 GMT  
		Size: 32.2 KB (32202 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:2844c11b4d09643d7d5b3a8164db05c2749c385069c298a6e5a35cad18026df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153238004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835854ca935b3f9df8ec7995b6580266b035c5a79c98ea1f886ee2722e021be5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533550fe86a6b67962a386a3bcb6dacd01a0ece569024db3237a636e9fd560dc`  
		Last Modified: Sat, 07 Sep 2024 08:26:28 GMT  
		Size: 37.9 MB (37925205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbf961e15bbd490960349ee83ec6f9ed91cfdbcff8486702cb71ce88dee9b6`  
		Last Modified: Sat, 07 Sep 2024 08:26:27 GMT  
		Size: 1.4 MB (1382246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d119284b0194114c441def36dffdf242f99ef680ccb28b62b0be8b54e28e0c`  
		Last Modified: Sat, 07 Sep 2024 08:26:27 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0df348f8d8a63c0aa3e3c903e3e8d2b47ad3ed22fa26873e43f4b59eb10d1`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 701.2 KB (701155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9706a6d81c33e5a28fde18100484d8f50d7a8739ea84f0946f424169efafc4e1`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 1.1 MB (1088897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e427acc0dd5b6182f6b5ab3165ab9f6a7b78778bb077f80eb92eedfda3ed3`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba8c8706c98baedd2e101ce98be3384372cccb36dc1d7f76ef10b0679b370e`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 10.9 MB (10860632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b8d4925ed8418e5e79700f12a3636b0ac1d8d03cdff2d9ffa6acca6790537`  
		Last Modified: Thu, 24 Oct 2024 23:13:43 GMT  
		Size: 98.4 MB (98351014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd81a0b9f2de2f08bfd81599174839195299731111c69ef44afceb04ea92e0`  
		Last Modified: Thu, 24 Oct 2024 23:13:40 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9521e25cbc50b349600e7b192c52b66240bbc19b6b2c7b023be1668afce6396c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3335854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a334ff5b7d7f264a1cba10c0f43c20d36492f1cc1d318fef85810af32413bd`

```dockerfile
```

-	Layers:
	-	`sha256:e63835dc34176b8f250f900fbff6d6c5254b6af05e8cb60a039d57c36fa7247b`  
		Last Modified: Thu, 24 Oct 2024 23:13:40 GMT  
		Size: 3.3 MB (3303437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14990ecb57e61732524decbbbc9931db1197b9750dced3e6fdb503a0fd903c1`  
		Last Modified: Thu, 24 Oct 2024 23:13:40 GMT  
		Size: 32.4 KB (32417 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:5ea1152bfbc527d19561bfb48407dd712babf83db0797c3d4d543ff792cce7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167307308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591ca707b241a0349e15cb4ceb51a459d78d2d45a4d9eb98d3e229c65b327dcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fb22222d09c03bb9af4878caea5b80f7e0fcfcce4b571670fac87d5eeeb0a`  
		Last Modified: Sat, 07 Sep 2024 08:17:56 GMT  
		Size: 39.5 MB (39537563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06bae4ce73dffe95558039a913bc68e99ac09e33310294fdf1816669403fbb4`  
		Last Modified: Sat, 07 Sep 2024 08:17:55 GMT  
		Size: 1.4 MB (1382246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34547485a12657cd5f8d0eb0e298d473be57651f97ffb7e0b79467eb6c7ca6f1`  
		Last Modified: Sat, 07 Sep 2024 08:17:54 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9292a9275cc1fbd2b075567da960d64f77e4a9a7981ae528d6a8cf67b9c72abd`  
		Last Modified: Tue, 08 Oct 2024 02:26:37 GMT  
		Size: 852.8 KB (852767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6fa99804430144f844f1df4501c3f39b3f5e868168b8d4ef8bd693f002cbf`  
		Last Modified: Tue, 08 Oct 2024 02:26:37 GMT  
		Size: 1.1 MB (1053464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5d7139c87d74e92064721cfacba41629b728a630bdd2c72e15b111922e3afd`  
		Last Modified: Wed, 23 Oct 2024 00:15:40 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd4808ecbda75572dbecdecc4d5c87ef736d46ed587f1af4b5f27640f23c163`  
		Last Modified: Wed, 23 Oct 2024 00:15:40 GMT  
		Size: 10.9 MB (10865263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6831bbf109db029746d0648670fcc8d301bea997d959d63e362fe8dfc61fcf3`  
		Last Modified: Thu, 24 Oct 2024 23:00:48 GMT  
		Size: 110.3 MB (110255704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58131a915e4da6739251a82ba69ae8a1d6136aadc0e4dc9a15bdd1ffe5839fd4`  
		Last Modified: Thu, 24 Oct 2024 23:00:45 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ca49a9329c4be56141f92be0453d5a601e23e109c63bd4515b272fc9cc9de222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bb34992508785d41bbc38fcb248411e7f479bc17cb9731d06fcc082cfc08b5`

```dockerfile
```

-	Layers:
	-	`sha256:d4a02bef7ceb4620acea2bf5649cd63196bd79ca8a84c176e58399e592103078`  
		Last Modified: Thu, 24 Oct 2024 23:00:45 GMT  
		Size: 3.3 MB (3311355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd2af3a8af6511633483f94ead1b1519df3f872c88bab1c4c216e949404001a`  
		Last Modified: Thu, 24 Oct 2024 23:00:45 GMT  
		Size: 32.5 KB (32456 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.98`

**does not exist** (yet?)

## `ghost:5.98-alpine`

**does not exist** (yet?)

## `ghost:5.98.0`

**does not exist** (yet?)

## `ghost:5.98.0-alpine`

**does not exist** (yet?)

## `ghost:alpine`

```console
$ docker pull ghost@sha256:0fb8d3976ee222fb705bd2de4b8e89946f7fa57e60e54163585c69d8c284ae19
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
$ docker pull ghost@sha256:399e925722b29cb4c9e0e96883da3055f8efb02b997e8020e60841da973adf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147612244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1e74b076553228bee1d1bb15eeafa68223a3c417b4aeba3087ce087a5e5b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5fa6889f28fd528156e3fe0e0a254be528df1dad2e1d2d0ab8cf11131a073d`  
		Last Modified: Fri, 06 Sep 2024 23:16:09 GMT  
		Size: 39.8 MB (39831152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a466315fb2612e923981687f8b8ceb89aa3831ce5224fd75351306a06c7a250`  
		Last Modified: Fri, 06 Sep 2024 23:16:04 GMT  
		Size: 1.4 MB (1382233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ceedeff43cf732f04ee25de7c5bd5c6e18ca1101e2cb89d3ec52e8a15731d2f`  
		Last Modified: Fri, 06 Sep 2024 23:16:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc878b6f56a450ba8fd393fe47b16a0915df0462f52af02dd131d6dca55f4a`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 776.0 KB (776015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55299a314d60873e29861cf074df16d0fa3d47b897f3b83a0ac103bd0ed32032`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 1.1 MB (1121670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f725d1039d87b072201e21cd2519dd7490309443f913e342669f52741059072`  
		Last Modified: Thu, 24 Oct 2024 22:57:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ab5c7f9549dadaa682048914f93f28a03d1acbec11055b61345575fff0ac4a`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 10.9 MB (10864602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a822ca004dd5fb2dbb250ad9368cf08207ee68e760bda86c19c0fed8b1deb8d`  
		Last Modified: Thu, 24 Oct 2024 22:58:00 GMT  
		Size: 90.2 MB (90215669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a8af326984964ef5659f84f11853823064140f03eae9615a1cefbb78ff9c25`  
		Last Modified: Thu, 24 Oct 2024 22:57:58 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b501ed704a68db7178e832c22462c4742c0187cbb6d2b164bd2d5130db181ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0345b1805ef4153a584b18cd74ea179b105dd0a3ce4c8c090b95e410a557b5`

```dockerfile
```

-	Layers:
	-	`sha256:cde9825d30052cc0fee8944e7b4d1e5890644db51d1e76e0820b84695681c553`  
		Last Modified: Thu, 24 Oct 2024 22:57:57 GMT  
		Size: 3.3 MB (3311299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd273a0f55ab0441b427a71bf5a888d2408ba0c67099458fbe3b032cad3f49d`  
		Last Modified: Thu, 24 Oct 2024 22:57:56 GMT  
		Size: 32.2 KB (32241 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:fa36d7694df570f7380ec4b4ed6b26b6c1b664046b5bcfca3a74290fe4f8575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154365221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb1fa36b282be069b39c1a7871c000779ffe5494b0e12bf72be49445b149f93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b1ff41b89689262f8588b245bb78190b8a0c16c16c9daf3cebb351bccfdb3`  
		Last Modified: Sat, 07 Sep 2024 07:52:14 GMT  
		Size: 38.4 MB (38420067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4959454224b256e3ad89e9e437a96ca021ed6f390eb5ad33a272adafbb2857e`  
		Last Modified: Sat, 07 Sep 2024 07:52:13 GMT  
		Size: 1.4 MB (1382249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f02e22fa6268f811fb76b6926a490d125499f220d5a7385ac2399517457f49`  
		Last Modified: Sat, 07 Sep 2024 07:52:12 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40680b97610532f1ca37d28c11bfaf7cb9abf82f7f7c24d7f700804314586c72`  
		Last Modified: Sat, 07 Sep 2024 13:37:46 GMT  
		Size: 767.8 KB (767845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7725ea60a425a96c96318772b1bf05da646a7064d297afa87dbc8f58ba5881e3`  
		Last Modified: Sat, 07 Sep 2024 13:37:46 GMT  
		Size: 1.1 MB (1088933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a28d0e08d8b5b681d01d146e049dd8b78d5ad3e2837d766e18f8910c77476`  
		Last Modified: Sat, 07 Sep 2024 13:37:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bf6e85286324b654be61b09098a1042e8f209a879bf1c64e4ddb451049e26b`  
		Last Modified: Sat, 07 Sep 2024 13:37:47 GMT  
		Size: 10.9 MB (10867259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b006d9ed2ae6cc2ca4f2ee6f765c91912fca4a97dbaceec4c7d67197ee919c`  
		Last Modified: Thu, 24 Oct 2024 23:08:22 GMT  
		Size: 98.7 MB (98661284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e95102f31da07ffe64952e7daf107b1f7fa499ffb4937d90c3eefa07a3a0fd6`  
		Last Modified: Thu, 24 Oct 2024 23:08:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:aeb42af488cdf5ca7b05e762ad6dfa7216f8efee5db8228d39bd3dfb09b5d218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3925360d54a904664af63d18bedf6424bb5e8498b60519020ebf4c6ceafa1fd5`

```dockerfile
```

-	Layers:
	-	`sha256:7db64ace60f845e77717a973846d3ab1c297ce6d1b0d588e4ae92a69263b3736`  
		Last Modified: Thu, 24 Oct 2024 23:08:19 GMT  
		Size: 32.2 KB (32202 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:2844c11b4d09643d7d5b3a8164db05c2749c385069c298a6e5a35cad18026df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153238004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835854ca935b3f9df8ec7995b6580266b035c5a79c98ea1f886ee2722e021be5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533550fe86a6b67962a386a3bcb6dacd01a0ece569024db3237a636e9fd560dc`  
		Last Modified: Sat, 07 Sep 2024 08:26:28 GMT  
		Size: 37.9 MB (37925205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbf961e15bbd490960349ee83ec6f9ed91cfdbcff8486702cb71ce88dee9b6`  
		Last Modified: Sat, 07 Sep 2024 08:26:27 GMT  
		Size: 1.4 MB (1382246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d119284b0194114c441def36dffdf242f99ef680ccb28b62b0be8b54e28e0c`  
		Last Modified: Sat, 07 Sep 2024 08:26:27 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0df348f8d8a63c0aa3e3c903e3e8d2b47ad3ed22fa26873e43f4b59eb10d1`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 701.2 KB (701155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9706a6d81c33e5a28fde18100484d8f50d7a8739ea84f0946f424169efafc4e1`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 1.1 MB (1088897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e427acc0dd5b6182f6b5ab3165ab9f6a7b78778bb077f80eb92eedfda3ed3`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba8c8706c98baedd2e101ce98be3384372cccb36dc1d7f76ef10b0679b370e`  
		Last Modified: Sat, 07 Sep 2024 14:20:27 GMT  
		Size: 10.9 MB (10860632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b8d4925ed8418e5e79700f12a3636b0ac1d8d03cdff2d9ffa6acca6790537`  
		Last Modified: Thu, 24 Oct 2024 23:13:43 GMT  
		Size: 98.4 MB (98351014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd81a0b9f2de2f08bfd81599174839195299731111c69ef44afceb04ea92e0`  
		Last Modified: Thu, 24 Oct 2024 23:13:40 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9521e25cbc50b349600e7b192c52b66240bbc19b6b2c7b023be1668afce6396c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3335854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a334ff5b7d7f264a1cba10c0f43c20d36492f1cc1d318fef85810af32413bd`

```dockerfile
```

-	Layers:
	-	`sha256:e63835dc34176b8f250f900fbff6d6c5254b6af05e8cb60a039d57c36fa7247b`  
		Last Modified: Thu, 24 Oct 2024 23:13:40 GMT  
		Size: 3.3 MB (3303437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14990ecb57e61732524decbbbc9931db1197b9750dced3e6fdb503a0fd903c1`  
		Last Modified: Thu, 24 Oct 2024 23:13:40 GMT  
		Size: 32.4 KB (32417 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:5ea1152bfbc527d19561bfb48407dd712babf83db0797c3d4d543ff792cce7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167307308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591ca707b241a0349e15cb4ceb51a459d78d2d45a4d9eb98d3e229c65b327dcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fb22222d09c03bb9af4878caea5b80f7e0fcfcce4b571670fac87d5eeeb0a`  
		Last Modified: Sat, 07 Sep 2024 08:17:56 GMT  
		Size: 39.5 MB (39537563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06bae4ce73dffe95558039a913bc68e99ac09e33310294fdf1816669403fbb4`  
		Last Modified: Sat, 07 Sep 2024 08:17:55 GMT  
		Size: 1.4 MB (1382246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34547485a12657cd5f8d0eb0e298d473be57651f97ffb7e0b79467eb6c7ca6f1`  
		Last Modified: Sat, 07 Sep 2024 08:17:54 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9292a9275cc1fbd2b075567da960d64f77e4a9a7981ae528d6a8cf67b9c72abd`  
		Last Modified: Tue, 08 Oct 2024 02:26:37 GMT  
		Size: 852.8 KB (852767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6fa99804430144f844f1df4501c3f39b3f5e868168b8d4ef8bd693f002cbf`  
		Last Modified: Tue, 08 Oct 2024 02:26:37 GMT  
		Size: 1.1 MB (1053464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5d7139c87d74e92064721cfacba41629b728a630bdd2c72e15b111922e3afd`  
		Last Modified: Wed, 23 Oct 2024 00:15:40 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd4808ecbda75572dbecdecc4d5c87ef736d46ed587f1af4b5f27640f23c163`  
		Last Modified: Wed, 23 Oct 2024 00:15:40 GMT  
		Size: 10.9 MB (10865263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6831bbf109db029746d0648670fcc8d301bea997d959d63e362fe8dfc61fcf3`  
		Last Modified: Thu, 24 Oct 2024 23:00:48 GMT  
		Size: 110.3 MB (110255704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58131a915e4da6739251a82ba69ae8a1d6136aadc0e4dc9a15bdd1ffe5839fd4`  
		Last Modified: Thu, 24 Oct 2024 23:00:45 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ca49a9329c4be56141f92be0453d5a601e23e109c63bd4515b272fc9cc9de222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bb34992508785d41bbc38fcb248411e7f479bc17cb9731d06fcc082cfc08b5`

```dockerfile
```

-	Layers:
	-	`sha256:d4a02bef7ceb4620acea2bf5649cd63196bd79ca8a84c176e58399e592103078`  
		Last Modified: Thu, 24 Oct 2024 23:00:45 GMT  
		Size: 3.3 MB (3311355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd2af3a8af6511633483f94ead1b1519df3f872c88bab1c4c216e949404001a`  
		Last Modified: Thu, 24 Oct 2024 23:00:45 GMT  
		Size: 32.5 KB (32456 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:37ed6c5f04ab1f0a93530b0dcb5a67a51985658f5941ed48fd69bc34d095a913
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
$ docker pull ghost@sha256:0dfea0340260b0bd3ab6de9a7ad399354899f15d9094b9876facc9f6db2755c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174389863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2505b202ad617a1a259f58e421d69e27c4aefaf6036ddbefee53086e6e0ce3d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36857b98621538ae167fc7e123b6fbeedf251abdf778478eaafe6b05832a29`  
		Last Modified: Thu, 17 Oct 2024 01:14:57 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f8c01c1aae756e37730cff35bd7a8397fdaef2891453596ec4fcb0ee04889b`  
		Last Modified: Thu, 17 Oct 2024 01:14:59 GMT  
		Size: 38.2 MB (38179242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3743e02f6e58d326658fb0c27c5211771e74e968dcbf3b8910a3ad6d6065d4c2`  
		Last Modified: Thu, 17 Oct 2024 01:14:57 GMT  
		Size: 1.7 MB (1708106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e8df9e7da85da17a9fc901fbe70e87ce70e9fe842e8dec211bf760448c518`  
		Last Modified: Thu, 17 Oct 2024 01:14:57 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b48401b588e559714a91a0632af8ba1aa9aadc8c84f93e4f3dc77d5f3f2e687`  
		Last Modified: Thu, 24 Oct 2024 22:58:08 GMT  
		Size: 1.4 MB (1444792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefc1693b4627148753751ded8ab16334caf86fe31656ddb4f9f07c2169c5a79`  
		Last Modified: Thu, 24 Oct 2024 22:58:08 GMT  
		Size: 10.9 MB (10865564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecfd7cfd3cfc918339635f56155c8addad60b3f30b78d9456a769d418a4fc7a`  
		Last Modified: Thu, 24 Oct 2024 22:58:09 GMT  
		Size: 93.1 MB (93061538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88015d884e1ea213e78f0cd0d18cfa6ec161322d643e98b97c8897e9eb89c6f`  
		Last Modified: Thu, 24 Oct 2024 22:58:07 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:bb4538f301bb3801bf029d06304a47d46ba1884ee775d8f81181f56283726b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a4c163bcd7e433f9548059410efd90f70b92664f4e70022a588e935769127a`

```dockerfile
```

-	Layers:
	-	`sha256:82a48b82f7f01c63bf7b5ac516fd45a7fd79876051f56ca690c44f5a974691b7`  
		Last Modified: Thu, 24 Oct 2024 22:58:07 GMT  
		Size: 5.4 MB (5420480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1f8a3c2b3124342ab1c38e55303f8ebd480222ee9a32ddcd614eb3770a77e7`  
		Last Modified: Thu, 24 Oct 2024 22:58:07 GMT  
		Size: 29.3 KB (29298 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8944e49ed2420db16af0bfd8044e0dd10791bbcbdaae063084b19fd64d0b98f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186914156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c7f8e097018230bf17c028fca14d798e1d45175a4fd00c9098633d012696d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c93bbfde48f5ab1bafbc7b40d95744dcda2249924d3bff15592f62991d91da`  
		Last Modified: Thu, 17 Oct 2024 14:29:28 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebe513cb685f99655a60ea2a5b1b0f3d9edb1eb05e647f12292cda6b2eba71`  
		Last Modified: Thu, 17 Oct 2024 14:44:08 GMT  
		Size: 34.8 MB (34834252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127a2d4461f22aa32723eebec9d751bada234cb9a3b16deb67991a87430d60e`  
		Last Modified: Thu, 17 Oct 2024 14:44:05 GMT  
		Size: 1.7 MB (1708447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e271a95e4ef89afbc4cfc2550ed87c190f21dce805b9fcf48c71b32939e44`  
		Last Modified: Thu, 17 Oct 2024 14:44:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a098602bac59119360ccade9f82e8cd50b545a24be30c0052fcefba78be607c2`  
		Last Modified: Fri, 18 Oct 2024 06:22:08 GMT  
		Size: 1.4 MB (1412473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd59287296a8abec277b55ab1ba1ba2c171de1880edadd5c71391c57f91e4e06`  
		Last Modified: Fri, 18 Oct 2024 06:22:08 GMT  
		Size: 10.9 MB (10865110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac490d1c26231444b96c3fe5df695c3771a7b8ea48e6fd5a846adf6e19946cda`  
		Last Modified: Thu, 24 Oct 2024 23:03:53 GMT  
		Size: 113.4 MB (113371348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e32200398d5cd0e9d805800c70a8a399e92f519debc1dfd46e58ff7ed33df1`  
		Last Modified: Thu, 24 Oct 2024 23:03:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:253995da89b748b007b7fca0afcd6da38a16327ae94546bd13823d91a5c52bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afd555d84539fe6bb85d63ab13490c90585bf466cf95e3a1806aa718a79ceaa`

```dockerfile
```

-	Layers:
	-	`sha256:fc3e104d5739490d4aa7eff43ed5cf8197d3306e8e7278d683919afd1ee773ba`  
		Last Modified: Thu, 24 Oct 2024 23:03:50 GMT  
		Size: 5.4 MB (5425949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2ffb7e6a00428970b70a2cf1df9c7cdfcd2403a64b8d65ee48f696eb53869b`  
		Last Modified: Thu, 24 Oct 2024 23:03:49 GMT  
		Size: 29.4 KB (29439 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:376624c3083268d6663cadaf896ae31e8ec628ff606d731add0a64e2354d449b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175358055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0ec6080215207ff2ff8a8cc8d7c96f79fea8d4d11ce0c46c0ebfe6c2c672b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ddb100d04a9a60ec43dd82c5f230e3f9a986af5a5d8b341cd2cb860f40c234`  
		Last Modified: Thu, 17 Oct 2024 13:36:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aef2c99b54eb40aaa69ff9b9ab139f0b510eff128f96b45b5beba014e9179a6`  
		Last Modified: Thu, 17 Oct 2024 13:49:16 GMT  
		Size: 38.2 MB (38223612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12af688d404f37010b8656e1ea189016adb20cae63fb49a4c34772f6e5f38882`  
		Last Modified: Thu, 17 Oct 2024 13:49:15 GMT  
		Size: 1.7 MB (1708292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d4419d49088625b08316adca0cb23bf97ca22872cec9c87189f1600ca8ca1d`  
		Last Modified: Thu, 17 Oct 2024 13:49:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656f7a269cf68f35ceeacf03cef909ee99440e93db9cb2fff5ac271598712df2`  
		Last Modified: Wed, 23 Oct 2024 00:11:25 GMT  
		Size: 1.4 MB (1376608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837843f7e3692a14b5c7e4491946f45ef5ebc099963dbf660dddf277b6cf129`  
		Last Modified: Wed, 23 Oct 2024 00:11:25 GMT  
		Size: 10.9 MB (10865809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9749d1d8f1a5d9af077eb35a9531d4c2e82d9731823a536b090b34de8bbe151`  
		Last Modified: Thu, 24 Oct 2024 22:57:02 GMT  
		Size: 94.0 MB (94023061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0dbe29cf7dfa8a68d363c1c08975fd255d17fe10a6c1ff0d08544d6d2c721`  
		Last Modified: Thu, 24 Oct 2024 22:56:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:8bfe9cd0f183dc8491fde9a512bdce10ac7db3059fcf4a208ca6431817cf8c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df33892c27fd824696f1de00498987e92d5b365873b766669c009c799b32571`

```dockerfile
```

-	Layers:
	-	`sha256:b9cacb90a05f7bafa38d23ddde663b0b42f68f962db9e22bdc83c09802d4d932`  
		Last Modified: Thu, 24 Oct 2024 22:57:00 GMT  
		Size: 5.4 MB (5420730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2617a8281cdedd6f06d416a62f3289ac6cc313d3e8ccd10647ade2243603d813`  
		Last Modified: Thu, 24 Oct 2024 22:56:59 GMT  
		Size: 29.5 KB (29468 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:b3f7dc92b242b2735af2326e5bfff5d9fb9e01f52591db50d71ebfbfbef22fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187931874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc15a39d015027190addf9ce0199834ad98dccd76d59029769e3033a2df631c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604818cf87f319cda069f9971e4eae9d29c0ae287449aa7f1402ffbf6fa34b37`  
		Last Modified: Thu, 17 Oct 2024 09:04:40 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37107ff641a94a678b22533233149d3284797c9f9965b6d5c5ec09ef1365432b`  
		Last Modified: Thu, 17 Oct 2024 09:14:52 GMT  
		Size: 40.3 MB (40263098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e51b720c48366d32b3e802e652d96f66446ec9c28bafe6d71b3e8266ad240c5`  
		Last Modified: Thu, 17 Oct 2024 09:14:51 GMT  
		Size: 1.7 MB (1708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a14799ac36d29c01aa65fbbdf2b86861553d005f04ee7d3f16b9a96385d01b`  
		Last Modified: Thu, 17 Oct 2024 09:14:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b653865e0124e1fe5807478369409216fb1c30fcfcae6f5778a0e413e4b1ab2c`  
		Last Modified: Wed, 23 Oct 2024 00:15:26 GMT  
		Size: 1.4 MB (1366548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49d5ff0c0b6859c18d854ac99ea20a0a27944076b84d87c5f987df9e11a02fc`  
		Last Modified: Wed, 23 Oct 2024 00:15:27 GMT  
		Size: 10.9 MB (10867095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ee32d15cd2ca283a5cfce8a4d073a147d5bdc897032df05fff66a85254a09b`  
		Last Modified: Thu, 24 Oct 2024 23:04:38 GMT  
		Size: 100.6 MB (100600271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa470a6fbea78a5b4f609a06f5c959638ade1430e2ceca757aab9385fc854b88`  
		Last Modified: Thu, 24 Oct 2024 23:04:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:289f0dcef973921469dc055ff16ea252705e5165e03d5e692c875f6cba59414a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf4280c5c3b8b588bf54be5b225967c1d0f1f476b7c87381617f8f02f380e2f`

```dockerfile
```

-	Layers:
	-	`sha256:717607b4c7f872a4922459ea715043ad51f40c160d7c3bd6d46634920e84757d`  
		Last Modified: Thu, 24 Oct 2024 23:04:35 GMT  
		Size: 5.4 MB (5416740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9af13cfc3f278bc713db187bfc88b652887e951e3f930309917aabf96957b61`  
		Last Modified: Thu, 24 Oct 2024 23:04:34 GMT  
		Size: 29.4 KB (29385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:3847c55dffb24323a48b5848b12f5178e742e1d5185598a83d7d1d299512f5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180443392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622970d8373ee1f9ebc8290d25c816cb44026dd12736daf61338fd105a88c771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 23 Oct 2024 14:19:12 GMT
ENV GHOST_VERSION=5.97.3
# Wed, 23 Oct 2024 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 23 Oct 2024 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 23 Oct 2024 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 23 Oct 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Oct 2024 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 23 Oct 2024 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9ccece114e5fd859788dca76e16273103e184aa5fded780b86d30f19feb07`  
		Last Modified: Thu, 17 Oct 2024 13:35:57 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988b585ca6b4a41eed6fc8de77520540958c4b357a1f90351d3025551d6232f8`  
		Last Modified: Thu, 17 Oct 2024 13:44:25 GMT  
		Size: 38.4 MB (38403852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7b5d7017150bc91aced99fb06b326881a9ce6a26f427cfc99ef3db2b0b0f2f`  
		Last Modified: Thu, 17 Oct 2024 13:44:22 GMT  
		Size: 1.7 MB (1708161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9f0c486693be660b5ec37260553c31acb00d8d4fda7289f034ee42cb777fc`  
		Last Modified: Thu, 17 Oct 2024 13:44:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7b3bd1710880e24c4eb7081acea7ff8099ae79aecdb2db33650fccb4d18555`  
		Last Modified: Thu, 17 Oct 2024 19:45:54 GMT  
		Size: 1.4 MB (1410060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a9a3a17c12ba6c739052563b18f443c49d0572fdca0ca4e8144ceccb7f81`  
		Last Modified: Wed, 23 Oct 2024 00:34:43 GMT  
		Size: 10.9 MB (10875398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc455ca987b5a1523f6992875be0655c0d875fe6efea915f4f2a8c2372b147`  
		Last Modified: Thu, 24 Oct 2024 23:12:29 GMT  
		Size: 100.6 MB (100551507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6617aa0598cc9ac91ba5eedee30c1f5da93948aa53b9a5587468d235dc3de8d0`  
		Last Modified: Thu, 24 Oct 2024 23:12:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:937f8bea2c63ccab0c1f70b53da29597573952dd46f127b13d5d241e2dbaa8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7385aca39d77f4f77fb66ae4ebc7a49c374f7ea9dd85c2920a7e2552b2db0284`

```dockerfile
```

-	Layers:
	-	`sha256:fdd65679fca91d9224c84d768eccf9b13434fc5c9cb8bff3e9589512ddf9cd35`  
		Last Modified: Thu, 24 Oct 2024 23:12:27 GMT  
		Size: 5.4 MB (5412214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d4b6fb293aa2b5000d13fd0be052891172e01028ae1e5145d04bb0e36eb4c1`  
		Last Modified: Thu, 24 Oct 2024 23:12:27 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.in-toto+json

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.130`](#ghost5130)
-	[`ghost:5.130-alpine`](#ghost5130-alpine)
-	[`ghost:5.130.5`](#ghost51305)
-	[`ghost:5.130.5-alpine`](#ghost51305-alpine)
-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6.4`](#ghost64)
-	[`ghost:6.4-alpine`](#ghost64-alpine)
-	[`ghost:6.4.0`](#ghost640)
-	[`ghost:6.4.0-alpine`](#ghost640-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:1234e3f8d92d6d4f163d6ca3556615249360ceafd3eaf0fc79678e5ddb50c7cf
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
$ docker pull ghost@sha256:c4ee582fcc90bd5a0507c8e8bd5a6f2f553a3839d43ba825a945cb020adca2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192356233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d996e8c20b18a93609ba0de1b948a92e491962c5b92fd66593a898018af870fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fd8b73b35fb02ae1e5d88d7916fd6ddf1c28abccbbaa0df081973a3fb7130`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc7a307e4f0c6f42db41a5ffd9710465d65364298660e8896e29bc43d01fc42`  
		Last Modified: Tue, 21 Oct 2025 01:49:34 GMT  
		Size: 41.0 MB (40977858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94d46bab1b3fd7caf99971b3795b37b9c7c96111b34c1c186b2ea1e1aa4788`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 1.7 MB (1712646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba2484b6190cd1003099cfb3640097846d7c5db4767c29595b5ee4f1f3743aa`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bc298a40b118a27ab724545f2e19302eff959f88f35b84e6f4927123a77112`  
		Last Modified: Tue, 21 Oct 2025 05:04:15 GMT  
		Size: 1.2 MB (1247431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf7d7f0f6f45d751c16859de4a620065407bab8c4e5a0324876cb53729bfd45`  
		Last Modified: Tue, 21 Oct 2025 05:04:16 GMT  
		Size: 11.1 MB (11092749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18697634e447fb12b87a46c0b0acdd254afe0fca57e91301a932dc798f2dd11`  
		Last Modified: Tue, 21 Oct 2025 05:04:21 GMT  
		Size: 109.1 MB (109092904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db8fcd8cd46fb8e0e1abaf84d5816dd2d9cfec1a63042d7421bd2af6397877`  
		Last Modified: Tue, 21 Oct 2025 05:04:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:9d9d62316c75f5a1bdcd2e1b3508d0ed2273cafff4aa653f67b883107ec2e037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a5d00ee07e11e9b2ecf643cf7ee6d22d0831da062c0a162491f5b0a59f4cbc`

```dockerfile
```

-	Layers:
	-	`sha256:d892507296e96e893140a6fa7b4eb07786adf5d0e980743b659e68ad5317abd2`  
		Last Modified: Tue, 21 Oct 2025 09:45:27 GMT  
		Size: 5.5 MB (5542247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a8d30a58add7dac555776bad85938bc65cd32320a8cca3ef44ce34ea86ae91`  
		Last Modified: Tue, 21 Oct 2025 09:45:27 GMT  
		Size: 29.0 KB (29013 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:740f94b84a82f155563d3b62516801ede6143994b5ff2606c3f46492f2d1b6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed0432f4d5074871fbf4fa8f01501a26a406786b9e043e0f8b488e2b4ea5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa5dd76bf6a6f628827ea559b60446744dfa9ade8b8f23103539f145d1a4f1`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056ef32d345e942bff6654bdf505b9dcf915a92ccea21365fc818658bc880b6d`  
		Last Modified: Tue, 21 Oct 2025 03:00:39 GMT  
		Size: 37.1 MB (37064241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f7e58a47465ac6218314d3afacdb7cf9ee9d6cfac8f2d78de6265541fd380b`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 1.7 MB (1712810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a101f7815b320aab8b3a95ba40fa3457c37bb4b55b6c00f677ef226fd092`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163c981f9857cefc82032e38ba4f8fa1e96d8c41ad0712a03b1f6ca8f9dff8b`  
		Last Modified: Tue, 21 Oct 2025 04:34:45 GMT  
		Size: 1.2 MB (1214271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26322b3cda6e43f06a15ca86bc874d1b02662079dc869cc75807f871df77a53`  
		Last Modified: Tue, 21 Oct 2025 04:34:46 GMT  
		Size: 11.1 MB (11094253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae88ec9a31f80538e41bbeb0ac9203161ae475a6c75f3fbf4775dd39e6324e2`  
		Last Modified: Tue, 21 Oct 2025 04:35:04 GMT  
		Size: 120.6 MB (120588778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72bb9490931f5cac309e2733aa2b51a3d45b7cb48658933af52e004a418a993`  
		Last Modified: Tue, 21 Oct 2025 04:34:44 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:86c6fcc62efad136f4605606abdfca35da46a9131d595c1f9fd49884f820279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10445a4759255c56a4377ed612b81678aa6f7ef1972bbdfb24f6a5427b600cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc261a11cd313b365d61bf9182b90adc5ededc1a05a157cf8792de9b967139dd`  
		Last Modified: Tue, 21 Oct 2025 09:45:32 GMT  
		Size: 5.5 MB (5545002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1981664eee99b8439855ffb8d0b7b9e318b2602d6f8fda168cb9652ee58371c`  
		Last Modified: Tue, 21 Oct 2025 09:45:33 GMT  
		Size: 29.1 KB (29112 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ae9d48ad1dbda46f77a2c72e6bb31b84a47f894e01161d949de354ef56e1d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192240574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed6c141d5f20f78b59e0e99f7f35e5a90f3db4ea6603abe22a9f0bb2826e57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bafef0543896231dab4096408462ad5fa340af4bb183ba0b4820dfab2b6f11`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a325c8dcfdfdc2ef98b317671620ed347d90e695636a97d5c7b5494b8131e4`  
		Last Modified: Tue, 21 Oct 2025 01:53:35 GMT  
		Size: 40.9 MB (40939677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5cce71776519d5c05085c48d3bfc8307161acc49e59ff407fd93e0dc563e74`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 1.7 MB (1712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef293a7c70c4590cdaa1590a59d5b98dcb0e7260b22c0f008e8d3226b38cebd1`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e1e7732807352ea11baff3cf4c0b9189f724c0405efdd509bb9670602398d8`  
		Last Modified: Tue, 21 Oct 2025 02:53:50 GMT  
		Size: 1.2 MB (1201379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f67f4cc22db589dcbecb9ddf26cc19b33ac83fb2255122a9a0efb0483383f0`  
		Last Modified: Tue, 21 Oct 2025 02:53:51 GMT  
		Size: 11.1 MB (11093632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c0aee50cf3e256c9fbd8514f7f990e9c81ac1f382567ac41d255aed9dc40c7`  
		Last Modified: Tue, 21 Oct 2025 02:53:57 GMT  
		Size: 109.2 MB (109186743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1bb39d3876e009024f4d320898210565566058ff45ce4ed22c6347e07ddf4f`  
		Last Modified: Tue, 21 Oct 2025 02:53:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:624e6022e981872396113286e479b765de8d22b8e7acb11ead11c15c3e527b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b39cdbef91329c2ee29ccba3e2fbc28cec080ea8a2d738055f0e2f0eb97bb4d`

```dockerfile
```

-	Layers:
	-	`sha256:588abe32bc03f45f57b747e1d65fb18b46370444543763af72b3fbcacc50546d`  
		Last Modified: Tue, 21 Oct 2025 09:45:37 GMT  
		Size: 5.5 MB (5542538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18bfc64080cff4475fee66c78ef6b52ff113cb53e6fef674897ccf5e0d98653`  
		Last Modified: Tue, 21 Oct 2025 09:45:38 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:c7aa3828366f311c64058d6d203541206ed5fa952812b6215cfab09fad5385a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213060939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cb0d53d37a068316319dbabcbece5b95d7d02cf38f7e58b47c9f1b6faba19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49411b36115a141bf59f6b22bd0cd982d28879042ba1fc9590fe2360cd462c65`  
		Last Modified: Tue, 30 Sep 2025 02:50:48 GMT  
		Size: 43.5 MB (43469518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5cf704332bc79893b3be28bfa869fdccc4bd00e5043208b6b0f101847681ae`  
		Last Modified: Tue, 30 Sep 2025 02:50:40 GMT  
		Size: 1.7 MB (1712724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e89b2fa244e2cbcfa51f40d9cd3866a9e4e1cfa828b674bef5c44d2011161`  
		Last Modified: Tue, 30 Sep 2025 02:50:40 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853a36b6365d8c55965ed3dc15cfa4cbf9edc32874da181eb51517bf34eea70`  
		Last Modified: Tue, 30 Sep 2025 17:53:24 GMT  
		Size: 1.2 MB (1206223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49825f2edcea9641bcf2e27687130dc18a2a738d91a413b69547ed191cb2058`  
		Last Modified: Tue, 30 Sep 2025 17:53:26 GMT  
		Size: 11.1 MB (11086253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1610e6478d3b317695b6ae4d2c26c9f4860c9ee5e489f7590b425306d4a9055e`  
		Last Modified: Fri, 10 Oct 2025 04:23:08 GMT  
		Size: 123.5 MB (123513194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea58b6d229119d13111ff08c64793d36c1f2febe2b340d04611d1a34bcf5fd`  
		Last Modified: Tue, 30 Sep 2025 17:53:24 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:0881c06cc40e6c73c93f31e7e751ee8642377301d186c786945f4f9531933fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5570357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a20ed9edc86e492a43cacd12cb80694708afcef8906a5b4389dbd9b9b51dff`

```dockerfile
```

-	Layers:
	-	`sha256:73e1777b43e2c2cb8b251388f0e2a03e0b14187bb9a63372ef36f494ec491749`  
		Last Modified: Wed, 01 Oct 2025 21:45:38 GMT  
		Size: 5.5 MB (5541301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b0b646496a06d70adeb1dbb32dc618d16a12978f8ddb8b8b11cbc229a72c26`  
		Last Modified: Wed, 01 Oct 2025 21:45:38 GMT  
		Size: 29.1 KB (29056 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:29d1500da6fae62cc215c1ee0dfbb9dd729033d295ea46a4772c413ee0b26942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204789809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5971a76fca9fdf9d0410a9ca3189e7b67a508625af2f39e08ee74308d832c757`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550501004cc268bf67499eca6f83dbf365f7382e75baad19cc26e1d84e3e0726`  
		Last Modified: Tue, 30 Sep 2025 03:32:29 GMT  
		Size: 41.2 MB (41222585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276778cc802de9cb54cb2a5963133940ac80d35a2bd4a22500e4854324c8dec0`  
		Last Modified: Tue, 30 Sep 2025 03:32:26 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02712495daaa9b63d2e09ae9f7aecbacda58d2640146086271dcbb89d4d5671e`  
		Last Modified: Tue, 30 Sep 2025 03:32:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501f1e5b4c28a0ed8f7d32e1de1f3359f38205ff6bb14148f3dbf3c18980ba5`  
		Last Modified: Tue, 30 Sep 2025 14:38:06 GMT  
		Size: 1.2 MB (1221132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cf1957c22cb882c4f66b0ede54e58ba77942138dfe768d31f2f227d791e66`  
		Last Modified: Tue, 30 Sep 2025 14:38:07 GMT  
		Size: 11.1 MB (11090077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a9683cf3406bd058f7f58f50bb3422fa131d8d4356c8c8215dccc7524fd5df`  
		Last Modified: Tue, 30 Sep 2025 14:38:16 GMT  
		Size: 122.7 MB (122654743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397e71bb2752beac98557a0dfcc3aa1a3e97f501b352842a140ba31edeac30e4`  
		Last Modified: Tue, 30 Sep 2025 14:38:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:47d01cfb65c0d8a54ba59900be1e9abe7fce58fa5391087d6df8d53457aff9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b036b3b3bb6a2148718a52325391e0d9729f2a7b301d8bf40d63fc3029f31c9`

```dockerfile
```

-	Layers:
	-	`sha256:4b1bced782e946fc7da63a2819f3f22880afde82395a5e460eedeaeff0c11ca9`  
		Last Modified: Wed, 01 Oct 2025 21:45:43 GMT  
		Size: 5.5 MB (5540600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df04ceaf3f37aca325ed49caa71e31af479d80fcd35550a1ef23b11d1bc0660`  
		Last Modified: Wed, 01 Oct 2025 21:45:44 GMT  
		Size: 29.0 KB (29014 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:9bad3472a563ef8a4c9c5da21a5d4162e66237bf8d812aeb761120203824b2a7
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
$ docker pull ghost@sha256:6a1cbedc4e8a1f920b56c9583e74cdffa151f91bb178415f506177e0a1eef151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166633944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e3b379e7328a7afe589338772db38410102ae46ce051f4983221127ea3220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087321cece4f408fdac87711c4c5c51945101848dffd8848840912c1fceb02c`  
		Last Modified: Wed, 08 Oct 2025 23:11:38 GMT  
		Size: 42.8 MB (42751185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbe8556258562779088bb23277d1d0b7e43fc6ddd52623166a2ac6d92bc73a`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c90aa7c8726728fa9d2e330254ef29381efbd566aaee9933c3113c26f20ce`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ad3e8151160fcaa52e5d6eb67da8bf28c867ad8592a3136ae86ddb36347b45`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e1ab3e9312e110f32f4f7ff3daf40623be152e70eae4a286f56648fd4309b`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 923.4 KB (923422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fadc3742560c97f7245c5f12bb0bd44bee78f25ed6a6c2ef1150e8466d7112`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f27f24bf616f18ef1aa3c644f8a13e9ec89020238fa72f18d1af256c1ee7b4`  
		Last Modified: Wed, 08 Oct 2025 23:51:38 GMT  
		Size: 11.1 MB (11086503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99f53439298641af10902c4a9a3069d36486329c651d018747503e18f359c74`  
		Last Modified: Wed, 08 Oct 2025 23:51:45 GMT  
		Size: 106.0 MB (106031560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21afd4082edec249aa95f45d78741257b82f3c2892571e19f67eabc8100251`  
		Last Modified: Wed, 08 Oct 2025 23:51:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a1c6c14ec3b92e974a4703eaa62a1dcb83b2a1d1c0fdc0e9c64da5396d83377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b87de6a02d0d296c269747e46b058bcd90642bdc00cf7180d0f1185f375ef`

```dockerfile
```

-	Layers:
	-	`sha256:12ac79857995491e6a36ad6d95c2c09921b90474ca0bd769223fe2d749f4e65e`  
		Last Modified: Thu, 09 Oct 2025 00:45:31 GMT  
		Size: 3.3 MB (3328342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e018180bcce90d4f0505d5808bcb9beaebcb110c5ad91bfd77f10f9100ab4aa`  
		Last Modified: Thu, 09 Oct 2025 00:45:32 GMT  
		Size: 32.0 KB (31982 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:67c7fcb26717da23bfa4ab8c82cb92f15e50170f562f0c596313edb2dadf9c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179230405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05ec3f7964cbf59a74f9296c00f955cbe838131e24a1ed99eceb714b2f8f6cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d208e9a50a7329a3e35cea3f84bee7bbc22d2c2601ba700f2a63a9023c82a7`  
		Last Modified: Wed, 08 Oct 2025 22:38:08 GMT  
		Size: 41.0 MB (41026810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5c30696b54e4ecc9c43973e38ea443b66050e399565f624665d8d7c21c1c1`  
		Last Modified: Wed, 08 Oct 2025 22:38:04 GMT  
		Size: 1.3 MB (1260562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8febffd7e97dc3ffb2e6df18dbcbc5aca8d0feddc6ef6010fc91df679840808f`  
		Last Modified: Wed, 08 Oct 2025 22:38:03 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34308f4bae5bd95af8098a76ebab8299a3e720100da45c238334fcc908d75c13`  
		Last Modified: Wed, 08 Oct 2025 23:45:29 GMT  
		Size: 766.1 KB (766084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb78cbcc71159749c57b6c461fdb7e9d5f7721b09b175f02b2aa41ee87cd2af`  
		Last Modified: Wed, 08 Oct 2025 23:45:29 GMT  
		Size: 889.1 KB (889103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a3567fa4bbc58c8fb0f671cc7ab5e82e9e1930612dbf4036aa7d2287bd89fa`  
		Last Modified: Wed, 08 Oct 2025 23:45:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a4813c4c3993b3a994d1385759b6b678d9cf84bd46679039567cac6edbe062`  
		Last Modified: Wed, 08 Oct 2025 23:45:31 GMT  
		Size: 11.1 MB (11091467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760b6b8e96941a87a863d8c3cbf36307980fe513ca3ad73613158cde6be3faf`  
		Last Modified: Wed, 08 Oct 2025 23:45:47 GMT  
		Size: 120.7 MB (120691113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2f5f297083659464d0367a11fd412513f4b1c7a4c0852eb34b956d3268c55b`  
		Last Modified: Wed, 08 Oct 2025 23:45:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4de26e132cf09cc6500f1da781b7425e9ca553e1626501567bf570b155ba9071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eedebe8685e9bd04b5374289b3e8a920ea50624db8abac0494cc8cadee755dc`

```dockerfile
```

-	Layers:
	-	`sha256:1f8c46bc792eab7146857ac1f11fa2703f4f6ea6ee7d0a9c502b2c0595fda79e`  
		Last Modified: Thu, 09 Oct 2025 00:45:36 GMT  
		Size: 31.9 KB (31891 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:ea8e288a99e65864c64c0be6c3c6b21e70c42d64a0ece2ae6c36d5ca49cbe93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178058964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef02a80946c10252a051fd6fa0e2e7e12f9d955cd9a3b7c91a866bc410f267`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ddd92de5f07c1fd33a64afd1cbabb5840c4e449dd6da165ac10f5a0fb238c`  
		Last Modified: Wed, 08 Oct 2025 22:42:19 GMT  
		Size: 40.5 MB (40486869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4add442d3c9e42ebd58d7d83b9103db17e87a7656a79dadf805e943daa6e7b`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601627ae0f3799d11ff0eab5243905454d298a89baf63ff8addbeefc2e650280`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c41da4d372534e2036c7ef10038338fd26eac5b14f72f0a8fcf6ededc2c454`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 701.5 KB (701474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b68839b5f4706c74092113715edc96c12dcc321a233517c5b5016363ada868`  
		Last Modified: Thu, 09 Oct 2025 00:00:28 GMT  
		Size: 889.1 KB (889091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c90337ec34923396097c918e72addf139cf6b5837bab4e4c9c179a645a01729`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5d537fcd5cdea4c8158f8735af6e5530278b206e83974875ce4176ec2defbf`  
		Last Modified: Thu, 09 Oct 2025 00:00:28 GMT  
		Size: 11.1 MB (11088706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1bd9e8c07839fcf3118343d18a818592c0ed4eb22ef95eb57d9ffd296a8adc`  
		Last Modified: Thu, 09 Oct 2025 00:00:36 GMT  
		Size: 120.4 MB (120409533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1716825a464fd293bcfea90d5143bd074872b43fee16b183f69046e55e7b8a31`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:106c7a4d6a1428c0b8912c1a367c7f0410ca0d1decd175864b823323001fff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3357461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5e1ebb6aef757ad94509729ef7936f76a36514c3a0868ffb2062d5c33b263d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b706ca7863b5aeefdf442c4fecb42e6b90ece0c2a16b910985990e137db2c6`  
		Last Modified: Thu, 09 Oct 2025 00:45:40 GMT  
		Size: 3.3 MB (3325355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4f94848abad19a4b79d3d242c26919096eb01825750321df9e67cf9876118`  
		Last Modified: Thu, 09 Oct 2025 00:45:41 GMT  
		Size: 32.1 KB (32106 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8df838271e23127a401c0d84d04d779d968d79c39fdad2eb54f4425c6e382cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186140964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced19546d759658338ebda9ee908ff81b958feafb3fd9ea0713412ae5feb3133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf91d8655fcee18b3e9f9030b88064039b4755089a4c98719432fe701c79c0c`  
		Last Modified: Wed, 08 Oct 2025 22:21:36 GMT  
		Size: 42.4 MB (42425600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52007d429cadef85012960983199c2efa60d5f88821d6e018387cc1ece4e5e93`  
		Last Modified: Wed, 08 Oct 2025 22:21:33 GMT  
		Size: 1.3 MB (1260577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8efc3601c5973cef196e124a98ceb07ba442e371d7be036143f0cded6bbcf`  
		Last Modified: Wed, 08 Oct 2025 22:21:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d35d7905cd53a61aa82e5fd4205cba53381389999aad0f5ff741b9dddf36709`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 838.6 KB (838565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc85f6d97b542422296206fe39ba19b0f918abe97827e21796c9310b1aed65`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 876.4 KB (876362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49bc0e13802ff6c1fb214262b1d87bc2afdab25b38e9eaeb320ab9b97056eb`  
		Last Modified: Wed, 08 Oct 2025 23:30:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caec29d269b14ad0b094625fa4b4b93fd93435e39e5f13e215e919e34c290f8`  
		Last Modified: Wed, 08 Oct 2025 23:30:37 GMT  
		Size: 11.1 MB (11085152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391780b98201e7f1693935b7e3e5d96ef92cb959a238b11cc102b8b2c6305a9`  
		Last Modified: Wed, 08 Oct 2025 23:30:41 GMT  
		Size: 125.5 MB (125515453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85af581cc1ed48b09a8fcc29f4b16a372434d5eb67847f98f4ebc0769fa209fe`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:93935bf390afc8ff99a5fb09b1893e30cd1fe0610b2b92414ed9bc5a2d594f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8607f439d05e7aa9872697a7137fd47ad97ee97ecf0142595106db951d964f1`

```dockerfile
```

-	Layers:
	-	`sha256:4abbe38a19f0906c19eca9900140f6b9e9275306130741fa4ca6e37257a805de`  
		Last Modified: Thu, 09 Oct 2025 00:45:46 GMT  
		Size: 3.3 MB (3328438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf9dc328ef8d487ec04e93a70f4fa9b72ac795bd5e93985bcf1462f5087f048`  
		Last Modified: Thu, 09 Oct 2025 00:45:47 GMT  
		Size: 32.1 KB (32134 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130`

```console
$ docker pull ghost@sha256:1234e3f8d92d6d4f163d6ca3556615249360ceafd3eaf0fc79678e5ddb50c7cf
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
$ docker pull ghost@sha256:c4ee582fcc90bd5a0507c8e8bd5a6f2f553a3839d43ba825a945cb020adca2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192356233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d996e8c20b18a93609ba0de1b948a92e491962c5b92fd66593a898018af870fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fd8b73b35fb02ae1e5d88d7916fd6ddf1c28abccbbaa0df081973a3fb7130`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc7a307e4f0c6f42db41a5ffd9710465d65364298660e8896e29bc43d01fc42`  
		Last Modified: Tue, 21 Oct 2025 01:49:34 GMT  
		Size: 41.0 MB (40977858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94d46bab1b3fd7caf99971b3795b37b9c7c96111b34c1c186b2ea1e1aa4788`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 1.7 MB (1712646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba2484b6190cd1003099cfb3640097846d7c5db4767c29595b5ee4f1f3743aa`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bc298a40b118a27ab724545f2e19302eff959f88f35b84e6f4927123a77112`  
		Last Modified: Tue, 21 Oct 2025 05:04:15 GMT  
		Size: 1.2 MB (1247431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf7d7f0f6f45d751c16859de4a620065407bab8c4e5a0324876cb53729bfd45`  
		Last Modified: Tue, 21 Oct 2025 05:04:16 GMT  
		Size: 11.1 MB (11092749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18697634e447fb12b87a46c0b0acdd254afe0fca57e91301a932dc798f2dd11`  
		Last Modified: Tue, 21 Oct 2025 05:04:21 GMT  
		Size: 109.1 MB (109092904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db8fcd8cd46fb8e0e1abaf84d5816dd2d9cfec1a63042d7421bd2af6397877`  
		Last Modified: Tue, 21 Oct 2025 05:04:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:9d9d62316c75f5a1bdcd2e1b3508d0ed2273cafff4aa653f67b883107ec2e037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a5d00ee07e11e9b2ecf643cf7ee6d22d0831da062c0a162491f5b0a59f4cbc`

```dockerfile
```

-	Layers:
	-	`sha256:d892507296e96e893140a6fa7b4eb07786adf5d0e980743b659e68ad5317abd2`  
		Last Modified: Tue, 21 Oct 2025 09:45:27 GMT  
		Size: 5.5 MB (5542247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a8d30a58add7dac555776bad85938bc65cd32320a8cca3ef44ce34ea86ae91`  
		Last Modified: Tue, 21 Oct 2025 09:45:27 GMT  
		Size: 29.0 KB (29013 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm variant v7

```console
$ docker pull ghost@sha256:740f94b84a82f155563d3b62516801ede6143994b5ff2606c3f46492f2d1b6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed0432f4d5074871fbf4fa8f01501a26a406786b9e043e0f8b488e2b4ea5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa5dd76bf6a6f628827ea559b60446744dfa9ade8b8f23103539f145d1a4f1`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056ef32d345e942bff6654bdf505b9dcf915a92ccea21365fc818658bc880b6d`  
		Last Modified: Tue, 21 Oct 2025 03:00:39 GMT  
		Size: 37.1 MB (37064241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f7e58a47465ac6218314d3afacdb7cf9ee9d6cfac8f2d78de6265541fd380b`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 1.7 MB (1712810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a101f7815b320aab8b3a95ba40fa3457c37bb4b55b6c00f677ef226fd092`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163c981f9857cefc82032e38ba4f8fa1e96d8c41ad0712a03b1f6ca8f9dff8b`  
		Last Modified: Tue, 21 Oct 2025 04:34:45 GMT  
		Size: 1.2 MB (1214271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26322b3cda6e43f06a15ca86bc874d1b02662079dc869cc75807f871df77a53`  
		Last Modified: Tue, 21 Oct 2025 04:34:46 GMT  
		Size: 11.1 MB (11094253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae88ec9a31f80538e41bbeb0ac9203161ae475a6c75f3fbf4775dd39e6324e2`  
		Last Modified: Tue, 21 Oct 2025 04:35:04 GMT  
		Size: 120.6 MB (120588778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72bb9490931f5cac309e2733aa2b51a3d45b7cb48658933af52e004a418a993`  
		Last Modified: Tue, 21 Oct 2025 04:34:44 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:86c6fcc62efad136f4605606abdfca35da46a9131d595c1f9fd49884f820279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10445a4759255c56a4377ed612b81678aa6f7ef1972bbdfb24f6a5427b600cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc261a11cd313b365d61bf9182b90adc5ededc1a05a157cf8792de9b967139dd`  
		Last Modified: Tue, 21 Oct 2025 09:45:32 GMT  
		Size: 5.5 MB (5545002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1981664eee99b8439855ffb8d0b7b9e318b2602d6f8fda168cb9652ee58371c`  
		Last Modified: Tue, 21 Oct 2025 09:45:33 GMT  
		Size: 29.1 KB (29112 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ae9d48ad1dbda46f77a2c72e6bb31b84a47f894e01161d949de354ef56e1d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192240574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed6c141d5f20f78b59e0e99f7f35e5a90f3db4ea6603abe22a9f0bb2826e57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bafef0543896231dab4096408462ad5fa340af4bb183ba0b4820dfab2b6f11`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a325c8dcfdfdc2ef98b317671620ed347d90e695636a97d5c7b5494b8131e4`  
		Last Modified: Tue, 21 Oct 2025 01:53:35 GMT  
		Size: 40.9 MB (40939677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5cce71776519d5c05085c48d3bfc8307161acc49e59ff407fd93e0dc563e74`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 1.7 MB (1712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef293a7c70c4590cdaa1590a59d5b98dcb0e7260b22c0f008e8d3226b38cebd1`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e1e7732807352ea11baff3cf4c0b9189f724c0405efdd509bb9670602398d8`  
		Last Modified: Tue, 21 Oct 2025 02:53:50 GMT  
		Size: 1.2 MB (1201379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f67f4cc22db589dcbecb9ddf26cc19b33ac83fb2255122a9a0efb0483383f0`  
		Last Modified: Tue, 21 Oct 2025 02:53:51 GMT  
		Size: 11.1 MB (11093632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c0aee50cf3e256c9fbd8514f7f990e9c81ac1f382567ac41d255aed9dc40c7`  
		Last Modified: Tue, 21 Oct 2025 02:53:57 GMT  
		Size: 109.2 MB (109186743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1bb39d3876e009024f4d320898210565566058ff45ce4ed22c6347e07ddf4f`  
		Last Modified: Tue, 21 Oct 2025 02:53:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:624e6022e981872396113286e479b765de8d22b8e7acb11ead11c15c3e527b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b39cdbef91329c2ee29ccba3e2fbc28cec080ea8a2d738055f0e2f0eb97bb4d`

```dockerfile
```

-	Layers:
	-	`sha256:588abe32bc03f45f57b747e1d65fb18b46370444543763af72b3fbcacc50546d`  
		Last Modified: Tue, 21 Oct 2025 09:45:37 GMT  
		Size: 5.5 MB (5542538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18bfc64080cff4475fee66c78ef6b52ff113cb53e6fef674897ccf5e0d98653`  
		Last Modified: Tue, 21 Oct 2025 09:45:38 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; ppc64le

```console
$ docker pull ghost@sha256:c7aa3828366f311c64058d6d203541206ed5fa952812b6215cfab09fad5385a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213060939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cb0d53d37a068316319dbabcbece5b95d7d02cf38f7e58b47c9f1b6faba19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49411b36115a141bf59f6b22bd0cd982d28879042ba1fc9590fe2360cd462c65`  
		Last Modified: Tue, 30 Sep 2025 02:50:48 GMT  
		Size: 43.5 MB (43469518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5cf704332bc79893b3be28bfa869fdccc4bd00e5043208b6b0f101847681ae`  
		Last Modified: Tue, 30 Sep 2025 02:50:40 GMT  
		Size: 1.7 MB (1712724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e89b2fa244e2cbcfa51f40d9cd3866a9e4e1cfa828b674bef5c44d2011161`  
		Last Modified: Tue, 30 Sep 2025 02:50:40 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853a36b6365d8c55965ed3dc15cfa4cbf9edc32874da181eb51517bf34eea70`  
		Last Modified: Tue, 30 Sep 2025 17:53:24 GMT  
		Size: 1.2 MB (1206223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49825f2edcea9641bcf2e27687130dc18a2a738d91a413b69547ed191cb2058`  
		Last Modified: Tue, 30 Sep 2025 17:53:26 GMT  
		Size: 11.1 MB (11086253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1610e6478d3b317695b6ae4d2c26c9f4860c9ee5e489f7590b425306d4a9055e`  
		Last Modified: Fri, 10 Oct 2025 04:23:08 GMT  
		Size: 123.5 MB (123513194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea58b6d229119d13111ff08c64793d36c1f2febe2b340d04611d1a34bcf5fd`  
		Last Modified: Tue, 30 Sep 2025 17:53:24 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:0881c06cc40e6c73c93f31e7e751ee8642377301d186c786945f4f9531933fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5570357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a20ed9edc86e492a43cacd12cb80694708afcef8906a5b4389dbd9b9b51dff`

```dockerfile
```

-	Layers:
	-	`sha256:73e1777b43e2c2cb8b251388f0e2a03e0b14187bb9a63372ef36f494ec491749`  
		Last Modified: Wed, 01 Oct 2025 21:45:38 GMT  
		Size: 5.5 MB (5541301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b0b646496a06d70adeb1dbb32dc618d16a12978f8ddb8b8b11cbc229a72c26`  
		Last Modified: Wed, 01 Oct 2025 21:45:38 GMT  
		Size: 29.1 KB (29056 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; s390x

```console
$ docker pull ghost@sha256:29d1500da6fae62cc215c1ee0dfbb9dd729033d295ea46a4772c413ee0b26942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204789809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5971a76fca9fdf9d0410a9ca3189e7b67a508625af2f39e08ee74308d832c757`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550501004cc268bf67499eca6f83dbf365f7382e75baad19cc26e1d84e3e0726`  
		Last Modified: Tue, 30 Sep 2025 03:32:29 GMT  
		Size: 41.2 MB (41222585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276778cc802de9cb54cb2a5963133940ac80d35a2bd4a22500e4854324c8dec0`  
		Last Modified: Tue, 30 Sep 2025 03:32:26 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02712495daaa9b63d2e09ae9f7aecbacda58d2640146086271dcbb89d4d5671e`  
		Last Modified: Tue, 30 Sep 2025 03:32:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501f1e5b4c28a0ed8f7d32e1de1f3359f38205ff6bb14148f3dbf3c18980ba5`  
		Last Modified: Tue, 30 Sep 2025 14:38:06 GMT  
		Size: 1.2 MB (1221132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cf1957c22cb882c4f66b0ede54e58ba77942138dfe768d31f2f227d791e66`  
		Last Modified: Tue, 30 Sep 2025 14:38:07 GMT  
		Size: 11.1 MB (11090077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a9683cf3406bd058f7f58f50bb3422fa131d8d4356c8c8215dccc7524fd5df`  
		Last Modified: Tue, 30 Sep 2025 14:38:16 GMT  
		Size: 122.7 MB (122654743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397e71bb2752beac98557a0dfcc3aa1a3e97f501b352842a140ba31edeac30e4`  
		Last Modified: Tue, 30 Sep 2025 14:38:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:47d01cfb65c0d8a54ba59900be1e9abe7fce58fa5391087d6df8d53457aff9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b036b3b3bb6a2148718a52325391e0d9729f2a7b301d8bf40d63fc3029f31c9`

```dockerfile
```

-	Layers:
	-	`sha256:4b1bced782e946fc7da63a2819f3f22880afde82395a5e460eedeaeff0c11ca9`  
		Last Modified: Wed, 01 Oct 2025 21:45:43 GMT  
		Size: 5.5 MB (5540600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df04ceaf3f37aca325ed49caa71e31af479d80fcd35550a1ef23b11d1bc0660`  
		Last Modified: Wed, 01 Oct 2025 21:45:44 GMT  
		Size: 29.0 KB (29014 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine`

```console
$ docker pull ghost@sha256:9bad3472a563ef8a4c9c5da21a5d4162e66237bf8d812aeb761120203824b2a7
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
$ docker pull ghost@sha256:6a1cbedc4e8a1f920b56c9583e74cdffa151f91bb178415f506177e0a1eef151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166633944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e3b379e7328a7afe589338772db38410102ae46ce051f4983221127ea3220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087321cece4f408fdac87711c4c5c51945101848dffd8848840912c1fceb02c`  
		Last Modified: Wed, 08 Oct 2025 23:11:38 GMT  
		Size: 42.8 MB (42751185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbe8556258562779088bb23277d1d0b7e43fc6ddd52623166a2ac6d92bc73a`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c90aa7c8726728fa9d2e330254ef29381efbd566aaee9933c3113c26f20ce`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ad3e8151160fcaa52e5d6eb67da8bf28c867ad8592a3136ae86ddb36347b45`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e1ab3e9312e110f32f4f7ff3daf40623be152e70eae4a286f56648fd4309b`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 923.4 KB (923422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fadc3742560c97f7245c5f12bb0bd44bee78f25ed6a6c2ef1150e8466d7112`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f27f24bf616f18ef1aa3c644f8a13e9ec89020238fa72f18d1af256c1ee7b4`  
		Last Modified: Wed, 08 Oct 2025 23:51:38 GMT  
		Size: 11.1 MB (11086503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99f53439298641af10902c4a9a3069d36486329c651d018747503e18f359c74`  
		Last Modified: Wed, 08 Oct 2025 23:51:45 GMT  
		Size: 106.0 MB (106031560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21afd4082edec249aa95f45d78741257b82f3c2892571e19f67eabc8100251`  
		Last Modified: Wed, 08 Oct 2025 23:51:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a1c6c14ec3b92e974a4703eaa62a1dcb83b2a1d1c0fdc0e9c64da5396d83377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b87de6a02d0d296c269747e46b058bcd90642bdc00cf7180d0f1185f375ef`

```dockerfile
```

-	Layers:
	-	`sha256:12ac79857995491e6a36ad6d95c2c09921b90474ca0bd769223fe2d749f4e65e`  
		Last Modified: Thu, 09 Oct 2025 00:45:31 GMT  
		Size: 3.3 MB (3328342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e018180bcce90d4f0505d5808bcb9beaebcb110c5ad91bfd77f10f9100ab4aa`  
		Last Modified: Thu, 09 Oct 2025 00:45:32 GMT  
		Size: 32.0 KB (31982 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:67c7fcb26717da23bfa4ab8c82cb92f15e50170f562f0c596313edb2dadf9c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179230405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05ec3f7964cbf59a74f9296c00f955cbe838131e24a1ed99eceb714b2f8f6cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d208e9a50a7329a3e35cea3f84bee7bbc22d2c2601ba700f2a63a9023c82a7`  
		Last Modified: Wed, 08 Oct 2025 22:38:08 GMT  
		Size: 41.0 MB (41026810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5c30696b54e4ecc9c43973e38ea443b66050e399565f624665d8d7c21c1c1`  
		Last Modified: Wed, 08 Oct 2025 22:38:04 GMT  
		Size: 1.3 MB (1260562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8febffd7e97dc3ffb2e6df18dbcbc5aca8d0feddc6ef6010fc91df679840808f`  
		Last Modified: Wed, 08 Oct 2025 22:38:03 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34308f4bae5bd95af8098a76ebab8299a3e720100da45c238334fcc908d75c13`  
		Last Modified: Wed, 08 Oct 2025 23:45:29 GMT  
		Size: 766.1 KB (766084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb78cbcc71159749c57b6c461fdb7e9d5f7721b09b175f02b2aa41ee87cd2af`  
		Last Modified: Wed, 08 Oct 2025 23:45:29 GMT  
		Size: 889.1 KB (889103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a3567fa4bbc58c8fb0f671cc7ab5e82e9e1930612dbf4036aa7d2287bd89fa`  
		Last Modified: Wed, 08 Oct 2025 23:45:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a4813c4c3993b3a994d1385759b6b678d9cf84bd46679039567cac6edbe062`  
		Last Modified: Wed, 08 Oct 2025 23:45:31 GMT  
		Size: 11.1 MB (11091467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760b6b8e96941a87a863d8c3cbf36307980fe513ca3ad73613158cde6be3faf`  
		Last Modified: Wed, 08 Oct 2025 23:45:47 GMT  
		Size: 120.7 MB (120691113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2f5f297083659464d0367a11fd412513f4b1c7a4c0852eb34b956d3268c55b`  
		Last Modified: Wed, 08 Oct 2025 23:45:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4de26e132cf09cc6500f1da781b7425e9ca553e1626501567bf570b155ba9071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eedebe8685e9bd04b5374289b3e8a920ea50624db8abac0494cc8cadee755dc`

```dockerfile
```

-	Layers:
	-	`sha256:1f8c46bc792eab7146857ac1f11fa2703f4f6ea6ee7d0a9c502b2c0595fda79e`  
		Last Modified: Thu, 09 Oct 2025 00:45:36 GMT  
		Size: 31.9 KB (31891 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:ea8e288a99e65864c64c0be6c3c6b21e70c42d64a0ece2ae6c36d5ca49cbe93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178058964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef02a80946c10252a051fd6fa0e2e7e12f9d955cd9a3b7c91a866bc410f267`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ddd92de5f07c1fd33a64afd1cbabb5840c4e449dd6da165ac10f5a0fb238c`  
		Last Modified: Wed, 08 Oct 2025 22:42:19 GMT  
		Size: 40.5 MB (40486869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4add442d3c9e42ebd58d7d83b9103db17e87a7656a79dadf805e943daa6e7b`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601627ae0f3799d11ff0eab5243905454d298a89baf63ff8addbeefc2e650280`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c41da4d372534e2036c7ef10038338fd26eac5b14f72f0a8fcf6ededc2c454`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 701.5 KB (701474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b68839b5f4706c74092113715edc96c12dcc321a233517c5b5016363ada868`  
		Last Modified: Thu, 09 Oct 2025 00:00:28 GMT  
		Size: 889.1 KB (889091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c90337ec34923396097c918e72addf139cf6b5837bab4e4c9c179a645a01729`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5d537fcd5cdea4c8158f8735af6e5530278b206e83974875ce4176ec2defbf`  
		Last Modified: Thu, 09 Oct 2025 00:00:28 GMT  
		Size: 11.1 MB (11088706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1bd9e8c07839fcf3118343d18a818592c0ed4eb22ef95eb57d9ffd296a8adc`  
		Last Modified: Thu, 09 Oct 2025 00:00:36 GMT  
		Size: 120.4 MB (120409533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1716825a464fd293bcfea90d5143bd074872b43fee16b183f69046e55e7b8a31`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:106c7a4d6a1428c0b8912c1a367c7f0410ca0d1decd175864b823323001fff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3357461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5e1ebb6aef757ad94509729ef7936f76a36514c3a0868ffb2062d5c33b263d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b706ca7863b5aeefdf442c4fecb42e6b90ece0c2a16b910985990e137db2c6`  
		Last Modified: Thu, 09 Oct 2025 00:45:40 GMT  
		Size: 3.3 MB (3325355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4f94848abad19a4b79d3d242c26919096eb01825750321df9e67cf9876118`  
		Last Modified: Thu, 09 Oct 2025 00:45:41 GMT  
		Size: 32.1 KB (32106 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8df838271e23127a401c0d84d04d779d968d79c39fdad2eb54f4425c6e382cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186140964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced19546d759658338ebda9ee908ff81b958feafb3fd9ea0713412ae5feb3133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf91d8655fcee18b3e9f9030b88064039b4755089a4c98719432fe701c79c0c`  
		Last Modified: Wed, 08 Oct 2025 22:21:36 GMT  
		Size: 42.4 MB (42425600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52007d429cadef85012960983199c2efa60d5f88821d6e018387cc1ece4e5e93`  
		Last Modified: Wed, 08 Oct 2025 22:21:33 GMT  
		Size: 1.3 MB (1260577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8efc3601c5973cef196e124a98ceb07ba442e371d7be036143f0cded6bbcf`  
		Last Modified: Wed, 08 Oct 2025 22:21:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d35d7905cd53a61aa82e5fd4205cba53381389999aad0f5ff741b9dddf36709`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 838.6 KB (838565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc85f6d97b542422296206fe39ba19b0f918abe97827e21796c9310b1aed65`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 876.4 KB (876362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49bc0e13802ff6c1fb214262b1d87bc2afdab25b38e9eaeb320ab9b97056eb`  
		Last Modified: Wed, 08 Oct 2025 23:30:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caec29d269b14ad0b094625fa4b4b93fd93435e39e5f13e215e919e34c290f8`  
		Last Modified: Wed, 08 Oct 2025 23:30:37 GMT  
		Size: 11.1 MB (11085152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391780b98201e7f1693935b7e3e5d96ef92cb959a238b11cc102b8b2c6305a9`  
		Last Modified: Wed, 08 Oct 2025 23:30:41 GMT  
		Size: 125.5 MB (125515453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85af581cc1ed48b09a8fcc29f4b16a372434d5eb67847f98f4ebc0769fa209fe`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:93935bf390afc8ff99a5fb09b1893e30cd1fe0610b2b92414ed9bc5a2d594f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8607f439d05e7aa9872697a7137fd47ad97ee97ecf0142595106db951d964f1`

```dockerfile
```

-	Layers:
	-	`sha256:4abbe38a19f0906c19eca9900140f6b9e9275306130741fa4ca6e37257a805de`  
		Last Modified: Thu, 09 Oct 2025 00:45:46 GMT  
		Size: 3.3 MB (3328438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf9dc328ef8d487ec04e93a70f4fa9b72ac795bd5e93985bcf1462f5087f048`  
		Last Modified: Thu, 09 Oct 2025 00:45:47 GMT  
		Size: 32.1 KB (32134 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5`

```console
$ docker pull ghost@sha256:1234e3f8d92d6d4f163d6ca3556615249360ceafd3eaf0fc79678e5ddb50c7cf
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

### `ghost:5.130.5` - linux; amd64

```console
$ docker pull ghost@sha256:c4ee582fcc90bd5a0507c8e8bd5a6f2f553a3839d43ba825a945cb020adca2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192356233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d996e8c20b18a93609ba0de1b948a92e491962c5b92fd66593a898018af870fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fd8b73b35fb02ae1e5d88d7916fd6ddf1c28abccbbaa0df081973a3fb7130`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc7a307e4f0c6f42db41a5ffd9710465d65364298660e8896e29bc43d01fc42`  
		Last Modified: Tue, 21 Oct 2025 01:49:34 GMT  
		Size: 41.0 MB (40977858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94d46bab1b3fd7caf99971b3795b37b9c7c96111b34c1c186b2ea1e1aa4788`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 1.7 MB (1712646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba2484b6190cd1003099cfb3640097846d7c5db4767c29595b5ee4f1f3743aa`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bc298a40b118a27ab724545f2e19302eff959f88f35b84e6f4927123a77112`  
		Last Modified: Tue, 21 Oct 2025 05:04:15 GMT  
		Size: 1.2 MB (1247431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf7d7f0f6f45d751c16859de4a620065407bab8c4e5a0324876cb53729bfd45`  
		Last Modified: Tue, 21 Oct 2025 05:04:16 GMT  
		Size: 11.1 MB (11092749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18697634e447fb12b87a46c0b0acdd254afe0fca57e91301a932dc798f2dd11`  
		Last Modified: Tue, 21 Oct 2025 05:04:21 GMT  
		Size: 109.1 MB (109092904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db8fcd8cd46fb8e0e1abaf84d5816dd2d9cfec1a63042d7421bd2af6397877`  
		Last Modified: Tue, 21 Oct 2025 05:04:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:9d9d62316c75f5a1bdcd2e1b3508d0ed2273cafff4aa653f67b883107ec2e037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a5d00ee07e11e9b2ecf643cf7ee6d22d0831da062c0a162491f5b0a59f4cbc`

```dockerfile
```

-	Layers:
	-	`sha256:d892507296e96e893140a6fa7b4eb07786adf5d0e980743b659e68ad5317abd2`  
		Last Modified: Tue, 21 Oct 2025 09:45:27 GMT  
		Size: 5.5 MB (5542247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a8d30a58add7dac555776bad85938bc65cd32320a8cca3ef44ce34ea86ae91`  
		Last Modified: Tue, 21 Oct 2025 09:45:27 GMT  
		Size: 29.0 KB (29013 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:740f94b84a82f155563d3b62516801ede6143994b5ff2606c3f46492f2d1b6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed0432f4d5074871fbf4fa8f01501a26a406786b9e043e0f8b488e2b4ea5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa5dd76bf6a6f628827ea559b60446744dfa9ade8b8f23103539f145d1a4f1`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056ef32d345e942bff6654bdf505b9dcf915a92ccea21365fc818658bc880b6d`  
		Last Modified: Tue, 21 Oct 2025 03:00:39 GMT  
		Size: 37.1 MB (37064241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f7e58a47465ac6218314d3afacdb7cf9ee9d6cfac8f2d78de6265541fd380b`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 1.7 MB (1712810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a101f7815b320aab8b3a95ba40fa3457c37bb4b55b6c00f677ef226fd092`  
		Last Modified: Tue, 21 Oct 2025 03:00:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163c981f9857cefc82032e38ba4f8fa1e96d8c41ad0712a03b1f6ca8f9dff8b`  
		Last Modified: Tue, 21 Oct 2025 04:34:45 GMT  
		Size: 1.2 MB (1214271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26322b3cda6e43f06a15ca86bc874d1b02662079dc869cc75807f871df77a53`  
		Last Modified: Tue, 21 Oct 2025 04:34:46 GMT  
		Size: 11.1 MB (11094253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae88ec9a31f80538e41bbeb0ac9203161ae475a6c75f3fbf4775dd39e6324e2`  
		Last Modified: Tue, 21 Oct 2025 04:35:04 GMT  
		Size: 120.6 MB (120588778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72bb9490931f5cac309e2733aa2b51a3d45b7cb48658933af52e004a418a993`  
		Last Modified: Tue, 21 Oct 2025 04:34:44 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:86c6fcc62efad136f4605606abdfca35da46a9131d595c1f9fd49884f820279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10445a4759255c56a4377ed612b81678aa6f7ef1972bbdfb24f6a5427b600cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc261a11cd313b365d61bf9182b90adc5ededc1a05a157cf8792de9b967139dd`  
		Last Modified: Tue, 21 Oct 2025 09:45:32 GMT  
		Size: 5.5 MB (5545002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1981664eee99b8439855ffb8d0b7b9e318b2602d6f8fda168cb9652ee58371c`  
		Last Modified: Tue, 21 Oct 2025 09:45:33 GMT  
		Size: 29.1 KB (29112 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ae9d48ad1dbda46f77a2c72e6bb31b84a47f894e01161d949de354ef56e1d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192240574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed6c141d5f20f78b59e0e99f7f35e5a90f3db4ea6603abe22a9f0bb2826e57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bafef0543896231dab4096408462ad5fa340af4bb183ba0b4820dfab2b6f11`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a325c8dcfdfdc2ef98b317671620ed347d90e695636a97d5c7b5494b8131e4`  
		Last Modified: Tue, 21 Oct 2025 01:53:35 GMT  
		Size: 40.9 MB (40939677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5cce71776519d5c05085c48d3bfc8307161acc49e59ff407fd93e0dc563e74`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 1.7 MB (1712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef293a7c70c4590cdaa1590a59d5b98dcb0e7260b22c0f008e8d3226b38cebd1`  
		Last Modified: Tue, 21 Oct 2025 01:53:32 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e1e7732807352ea11baff3cf4c0b9189f724c0405efdd509bb9670602398d8`  
		Last Modified: Tue, 21 Oct 2025 02:53:50 GMT  
		Size: 1.2 MB (1201379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f67f4cc22db589dcbecb9ddf26cc19b33ac83fb2255122a9a0efb0483383f0`  
		Last Modified: Tue, 21 Oct 2025 02:53:51 GMT  
		Size: 11.1 MB (11093632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c0aee50cf3e256c9fbd8514f7f990e9c81ac1f382567ac41d255aed9dc40c7`  
		Last Modified: Tue, 21 Oct 2025 02:53:57 GMT  
		Size: 109.2 MB (109186743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1bb39d3876e009024f4d320898210565566058ff45ce4ed22c6347e07ddf4f`  
		Last Modified: Tue, 21 Oct 2025 02:53:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:624e6022e981872396113286e479b765de8d22b8e7acb11ead11c15c3e527b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b39cdbef91329c2ee29ccba3e2fbc28cec080ea8a2d738055f0e2f0eb97bb4d`

```dockerfile
```

-	Layers:
	-	`sha256:588abe32bc03f45f57b747e1d65fb18b46370444543763af72b3fbcacc50546d`  
		Last Modified: Tue, 21 Oct 2025 09:45:37 GMT  
		Size: 5.5 MB (5542538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18bfc64080cff4475fee66c78ef6b52ff113cb53e6fef674897ccf5e0d98653`  
		Last Modified: Tue, 21 Oct 2025 09:45:38 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; ppc64le

```console
$ docker pull ghost@sha256:c7aa3828366f311c64058d6d203541206ed5fa952812b6215cfab09fad5385a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213060939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cb0d53d37a068316319dbabcbece5b95d7d02cf38f7e58b47c9f1b6faba19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49411b36115a141bf59f6b22bd0cd982d28879042ba1fc9590fe2360cd462c65`  
		Last Modified: Tue, 30 Sep 2025 02:50:48 GMT  
		Size: 43.5 MB (43469518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5cf704332bc79893b3be28bfa869fdccc4bd00e5043208b6b0f101847681ae`  
		Last Modified: Tue, 30 Sep 2025 02:50:40 GMT  
		Size: 1.7 MB (1712724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e89b2fa244e2cbcfa51f40d9cd3866a9e4e1cfa828b674bef5c44d2011161`  
		Last Modified: Tue, 30 Sep 2025 02:50:40 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853a36b6365d8c55965ed3dc15cfa4cbf9edc32874da181eb51517bf34eea70`  
		Last Modified: Tue, 30 Sep 2025 17:53:24 GMT  
		Size: 1.2 MB (1206223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49825f2edcea9641bcf2e27687130dc18a2a738d91a413b69547ed191cb2058`  
		Last Modified: Tue, 30 Sep 2025 17:53:26 GMT  
		Size: 11.1 MB (11086253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1610e6478d3b317695b6ae4d2c26c9f4860c9ee5e489f7590b425306d4a9055e`  
		Last Modified: Fri, 10 Oct 2025 04:23:08 GMT  
		Size: 123.5 MB (123513194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea58b6d229119d13111ff08c64793d36c1f2febe2b340d04611d1a34bcf5fd`  
		Last Modified: Tue, 30 Sep 2025 17:53:24 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:0881c06cc40e6c73c93f31e7e751ee8642377301d186c786945f4f9531933fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5570357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a20ed9edc86e492a43cacd12cb80694708afcef8906a5b4389dbd9b9b51dff`

```dockerfile
```

-	Layers:
	-	`sha256:73e1777b43e2c2cb8b251388f0e2a03e0b14187bb9a63372ef36f494ec491749`  
		Last Modified: Wed, 01 Oct 2025 21:45:38 GMT  
		Size: 5.5 MB (5541301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b0b646496a06d70adeb1dbb32dc618d16a12978f8ddb8b8b11cbc229a72c26`  
		Last Modified: Wed, 01 Oct 2025 21:45:38 GMT  
		Size: 29.1 KB (29056 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; s390x

```console
$ docker pull ghost@sha256:29d1500da6fae62cc215c1ee0dfbb9dd729033d295ea46a4772c413ee0b26942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204789809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5971a76fca9fdf9d0410a9ca3189e7b67a508625af2f39e08ee74308d832c757`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550501004cc268bf67499eca6f83dbf365f7382e75baad19cc26e1d84e3e0726`  
		Last Modified: Tue, 30 Sep 2025 03:32:29 GMT  
		Size: 41.2 MB (41222585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276778cc802de9cb54cb2a5963133940ac80d35a2bd4a22500e4854324c8dec0`  
		Last Modified: Tue, 30 Sep 2025 03:32:26 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02712495daaa9b63d2e09ae9f7aecbacda58d2640146086271dcbb89d4d5671e`  
		Last Modified: Tue, 30 Sep 2025 03:32:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501f1e5b4c28a0ed8f7d32e1de1f3359f38205ff6bb14148f3dbf3c18980ba5`  
		Last Modified: Tue, 30 Sep 2025 14:38:06 GMT  
		Size: 1.2 MB (1221132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cf1957c22cb882c4f66b0ede54e58ba77942138dfe768d31f2f227d791e66`  
		Last Modified: Tue, 30 Sep 2025 14:38:07 GMT  
		Size: 11.1 MB (11090077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a9683cf3406bd058f7f58f50bb3422fa131d8d4356c8c8215dccc7524fd5df`  
		Last Modified: Tue, 30 Sep 2025 14:38:16 GMT  
		Size: 122.7 MB (122654743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397e71bb2752beac98557a0dfcc3aa1a3e97f501b352842a140ba31edeac30e4`  
		Last Modified: Tue, 30 Sep 2025 14:38:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:47d01cfb65c0d8a54ba59900be1e9abe7fce58fa5391087d6df8d53457aff9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b036b3b3bb6a2148718a52325391e0d9729f2a7b301d8bf40d63fc3029f31c9`

```dockerfile
```

-	Layers:
	-	`sha256:4b1bced782e946fc7da63a2819f3f22880afde82395a5e460eedeaeff0c11ca9`  
		Last Modified: Wed, 01 Oct 2025 21:45:43 GMT  
		Size: 5.5 MB (5540600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df04ceaf3f37aca325ed49caa71e31af479d80fcd35550a1ef23b11d1bc0660`  
		Last Modified: Wed, 01 Oct 2025 21:45:44 GMT  
		Size: 29.0 KB (29014 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-alpine`

```console
$ docker pull ghost@sha256:9bad3472a563ef8a4c9c5da21a5d4162e66237bf8d812aeb761120203824b2a7
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

### `ghost:5.130.5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:6a1cbedc4e8a1f920b56c9583e74cdffa151f91bb178415f506177e0a1eef151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166633944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e3b379e7328a7afe589338772db38410102ae46ce051f4983221127ea3220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087321cece4f408fdac87711c4c5c51945101848dffd8848840912c1fceb02c`  
		Last Modified: Wed, 08 Oct 2025 23:11:38 GMT  
		Size: 42.8 MB (42751185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbe8556258562779088bb23277d1d0b7e43fc6ddd52623166a2ac6d92bc73a`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c90aa7c8726728fa9d2e330254ef29381efbd566aaee9933c3113c26f20ce`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ad3e8151160fcaa52e5d6eb67da8bf28c867ad8592a3136ae86ddb36347b45`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e1ab3e9312e110f32f4f7ff3daf40623be152e70eae4a286f56648fd4309b`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 923.4 KB (923422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fadc3742560c97f7245c5f12bb0bd44bee78f25ed6a6c2ef1150e8466d7112`  
		Last Modified: Wed, 08 Oct 2025 23:51:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f27f24bf616f18ef1aa3c644f8a13e9ec89020238fa72f18d1af256c1ee7b4`  
		Last Modified: Wed, 08 Oct 2025 23:51:38 GMT  
		Size: 11.1 MB (11086503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99f53439298641af10902c4a9a3069d36486329c651d018747503e18f359c74`  
		Last Modified: Wed, 08 Oct 2025 23:51:45 GMT  
		Size: 106.0 MB (106031560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21afd4082edec249aa95f45d78741257b82f3c2892571e19f67eabc8100251`  
		Last Modified: Wed, 08 Oct 2025 23:51:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a1c6c14ec3b92e974a4703eaa62a1dcb83b2a1d1c0fdc0e9c64da5396d83377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b87de6a02d0d296c269747e46b058bcd90642bdc00cf7180d0f1185f375ef`

```dockerfile
```

-	Layers:
	-	`sha256:12ac79857995491e6a36ad6d95c2c09921b90474ca0bd769223fe2d749f4e65e`  
		Last Modified: Thu, 09 Oct 2025 00:45:31 GMT  
		Size: 3.3 MB (3328342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e018180bcce90d4f0505d5808bcb9beaebcb110c5ad91bfd77f10f9100ab4aa`  
		Last Modified: Thu, 09 Oct 2025 00:45:32 GMT  
		Size: 32.0 KB (31982 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:67c7fcb26717da23bfa4ab8c82cb92f15e50170f562f0c596313edb2dadf9c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179230405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05ec3f7964cbf59a74f9296c00f955cbe838131e24a1ed99eceb714b2f8f6cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d208e9a50a7329a3e35cea3f84bee7bbc22d2c2601ba700f2a63a9023c82a7`  
		Last Modified: Wed, 08 Oct 2025 22:38:08 GMT  
		Size: 41.0 MB (41026810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5c30696b54e4ecc9c43973e38ea443b66050e399565f624665d8d7c21c1c1`  
		Last Modified: Wed, 08 Oct 2025 22:38:04 GMT  
		Size: 1.3 MB (1260562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8febffd7e97dc3ffb2e6df18dbcbc5aca8d0feddc6ef6010fc91df679840808f`  
		Last Modified: Wed, 08 Oct 2025 22:38:03 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34308f4bae5bd95af8098a76ebab8299a3e720100da45c238334fcc908d75c13`  
		Last Modified: Wed, 08 Oct 2025 23:45:29 GMT  
		Size: 766.1 KB (766084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb78cbcc71159749c57b6c461fdb7e9d5f7721b09b175f02b2aa41ee87cd2af`  
		Last Modified: Wed, 08 Oct 2025 23:45:29 GMT  
		Size: 889.1 KB (889103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a3567fa4bbc58c8fb0f671cc7ab5e82e9e1930612dbf4036aa7d2287bd89fa`  
		Last Modified: Wed, 08 Oct 2025 23:45:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a4813c4c3993b3a994d1385759b6b678d9cf84bd46679039567cac6edbe062`  
		Last Modified: Wed, 08 Oct 2025 23:45:31 GMT  
		Size: 11.1 MB (11091467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760b6b8e96941a87a863d8c3cbf36307980fe513ca3ad73613158cde6be3faf`  
		Last Modified: Wed, 08 Oct 2025 23:45:47 GMT  
		Size: 120.7 MB (120691113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2f5f297083659464d0367a11fd412513f4b1c7a4c0852eb34b956d3268c55b`  
		Last Modified: Wed, 08 Oct 2025 23:45:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4de26e132cf09cc6500f1da781b7425e9ca553e1626501567bf570b155ba9071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eedebe8685e9bd04b5374289b3e8a920ea50624db8abac0494cc8cadee755dc`

```dockerfile
```

-	Layers:
	-	`sha256:1f8c46bc792eab7146857ac1f11fa2703f4f6ea6ee7d0a9c502b2c0595fda79e`  
		Last Modified: Thu, 09 Oct 2025 00:45:36 GMT  
		Size: 31.9 KB (31891 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:ea8e288a99e65864c64c0be6c3c6b21e70c42d64a0ece2ae6c36d5ca49cbe93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178058964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef02a80946c10252a051fd6fa0e2e7e12f9d955cd9a3b7c91a866bc410f267`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ddd92de5f07c1fd33a64afd1cbabb5840c4e449dd6da165ac10f5a0fb238c`  
		Last Modified: Wed, 08 Oct 2025 22:42:19 GMT  
		Size: 40.5 MB (40486869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4add442d3c9e42ebd58d7d83b9103db17e87a7656a79dadf805e943daa6e7b`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601627ae0f3799d11ff0eab5243905454d298a89baf63ff8addbeefc2e650280`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c41da4d372534e2036c7ef10038338fd26eac5b14f72f0a8fcf6ededc2c454`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 701.5 KB (701474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b68839b5f4706c74092113715edc96c12dcc321a233517c5b5016363ada868`  
		Last Modified: Thu, 09 Oct 2025 00:00:28 GMT  
		Size: 889.1 KB (889091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c90337ec34923396097c918e72addf139cf6b5837bab4e4c9c179a645a01729`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5d537fcd5cdea4c8158f8735af6e5530278b206e83974875ce4176ec2defbf`  
		Last Modified: Thu, 09 Oct 2025 00:00:28 GMT  
		Size: 11.1 MB (11088706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1bd9e8c07839fcf3118343d18a818592c0ed4eb22ef95eb57d9ffd296a8adc`  
		Last Modified: Thu, 09 Oct 2025 00:00:36 GMT  
		Size: 120.4 MB (120409533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1716825a464fd293bcfea90d5143bd074872b43fee16b183f69046e55e7b8a31`  
		Last Modified: Thu, 09 Oct 2025 00:00:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:106c7a4d6a1428c0b8912c1a367c7f0410ca0d1decd175864b823323001fff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3357461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5e1ebb6aef757ad94509729ef7936f76a36514c3a0868ffb2062d5c33b263d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b706ca7863b5aeefdf442c4fecb42e6b90ece0c2a16b910985990e137db2c6`  
		Last Modified: Thu, 09 Oct 2025 00:45:40 GMT  
		Size: 3.3 MB (3325355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4f94848abad19a4b79d3d242c26919096eb01825750321df9e67cf9876118`  
		Last Modified: Thu, 09 Oct 2025 00:45:41 GMT  
		Size: 32.1 KB (32106 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8df838271e23127a401c0d84d04d779d968d79c39fdad2eb54f4425c6e382cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186140964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced19546d759658338ebda9ee908ff81b958feafb3fd9ea0713412ae5feb3133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 03 Sep 2025 19:47:58 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
# Tue, 23 Sep 2025 19:29:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV NODE_ENV=production
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Sep 2025 19:29:19 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 23 Sep 2025 19:29:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Sep 2025 19:29:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Sep 2025 19:29:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Sep 2025 19:29:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:29:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 23 Sep 2025 19:29:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf91d8655fcee18b3e9f9030b88064039b4755089a4c98719432fe701c79c0c`  
		Last Modified: Wed, 08 Oct 2025 22:21:36 GMT  
		Size: 42.4 MB (42425600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52007d429cadef85012960983199c2efa60d5f88821d6e018387cc1ece4e5e93`  
		Last Modified: Wed, 08 Oct 2025 22:21:33 GMT  
		Size: 1.3 MB (1260577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8efc3601c5973cef196e124a98ceb07ba442e371d7be036143f0cded6bbcf`  
		Last Modified: Wed, 08 Oct 2025 22:21:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d35d7905cd53a61aa82e5fd4205cba53381389999aad0f5ff741b9dddf36709`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 838.6 KB (838565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc85f6d97b542422296206fe39ba19b0f918abe97827e21796c9310b1aed65`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 876.4 KB (876362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49bc0e13802ff6c1fb214262b1d87bc2afdab25b38e9eaeb320ab9b97056eb`  
		Last Modified: Wed, 08 Oct 2025 23:30:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caec29d269b14ad0b094625fa4b4b93fd93435e39e5f13e215e919e34c290f8`  
		Last Modified: Wed, 08 Oct 2025 23:30:37 GMT  
		Size: 11.1 MB (11085152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391780b98201e7f1693935b7e3e5d96ef92cb959a238b11cc102b8b2c6305a9`  
		Last Modified: Wed, 08 Oct 2025 23:30:41 GMT  
		Size: 125.5 MB (125515453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85af581cc1ed48b09a8fcc29f4b16a372434d5eb67847f98f4ebc0769fa209fe`  
		Last Modified: Wed, 08 Oct 2025 23:30:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:93935bf390afc8ff99a5fb09b1893e30cd1fe0610b2b92414ed9bc5a2d594f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8607f439d05e7aa9872697a7137fd47ad97ee97ecf0142595106db951d964f1`

```dockerfile
```

-	Layers:
	-	`sha256:4abbe38a19f0906c19eca9900140f6b9e9275306130741fa4ca6e37257a805de`  
		Last Modified: Thu, 09 Oct 2025 00:45:46 GMT  
		Size: 3.3 MB (3328438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf9dc328ef8d487ec04e93a70f4fa9b72ac795bd5e93985bcf1462f5087f048`  
		Last Modified: Thu, 09 Oct 2025 00:45:47 GMT  
		Size: 32.1 KB (32134 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6`

```console
$ docker pull ghost@sha256:7686d30f30383bb08df0dcd5c89fd897c4e2112d3f6a50f8ecdb78cf021bad2e
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
$ docker pull ghost@sha256:e0d477eca26277b7868de615763a27a8d75724bebdc72f8e42ba716d7d5f133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218576394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c46db0139e218d0602cd5e87b8e96145de5fa8a722502670a1eac235387378f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98ba22ffba63e671e794151a8c72b2dd2e2394a99dfdadb48375658423035c`  
		Last Modified: Tue, 21 Oct 2025 01:49:16 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce3834b70636fccfd15681ae09efc245e61d942555ff1b60eff662498f71f8`  
		Last Modified: Tue, 21 Oct 2025 01:49:20 GMT  
		Size: 49.4 MB (49406240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4168ab2bca6183681fd3571770924ab57da32eadefdb46f2208e8d8e572011`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e85ddc713935ca5a0accf8aec281f24ed3e23d93f11df909657e9ee9a0403`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184228eff12de998e31c119c22628a0214103d642cb2565a8f3e8f63f443bb1`  
		Last Modified: Tue, 21 Oct 2025 05:05:15 GMT  
		Size: 1.2 MB (1247341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3edd59bde935bd9eb92e8a1d7062f172dff05ee19bd9154471d701aa16affd9`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 11.7 MB (11661483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46bdfee218799cc3f27d6745d89a93a4047bf50be50e3e2ee83cd465d74fc52`  
		Last Modified: Tue, 21 Oct 2025 05:05:23 GMT  
		Size: 126.3 MB (126316069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63b4f25f0e618fed546bcd79af50eaa4e82811670015b2e7e0a784fddb26d21`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:6f4e0d84f80c4c7af9ea51d490fb0a102070b88740f56050d19d6d6cd3b9927e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4ac880fa060e58864e38bfa6a08c0084a3f01ca86672c61cdba47104730bf`

```dockerfile
```

-	Layers:
	-	`sha256:e7d16010c082e36f6352e043cc8ad362b86ee7ce147b43037b74ebbdf9e48814`  
		Last Modified: Tue, 21 Oct 2025 09:45:47 GMT  
		Size: 5.6 MB (5553963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0aa203325540398a2d4bb16fb5c221dc12e68ee0752c49dec8160b877b0c09`  
		Last Modified: Tue, 21 Oct 2025 09:45:48 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a8d79fc46cfa3b2146fa9fdd21dfb3b7268ba7494cd810b3ffe794d580823271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210030395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26bf23785bc61c442262280e3ac6923f91b3c3a6d757abe11c45c98aa1dae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b71629629a04cc6e17d182034fdc2181577adfa385f1edbfc4dd8bc3d17a38a`  
		Last Modified: Tue, 21 Oct 2025 02:57:36 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b787ce0420c13b5936470725c1246c0a56bb1980f368545047829b37396961`  
		Last Modified: Tue, 21 Oct 2025 02:57:38 GMT  
		Size: 44.1 MB (44136924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ab4cac8e6724a34f622a34a9016e857f8280ad0ec6152728226d371344e12`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 1.7 MB (1712852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e3d58d86740d69693dd91be91201911df44b63d9904f076ebe3cb30c5e100`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636d5fe8a91c198d3cec1a0f69391c7eddc5173ef352005fb1b98d5931561b7`  
		Last Modified: Tue, 21 Oct 2025 04:34:23 GMT  
		Size: 1.2 MB (1214242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12442508853d21a7948b51aeaac6c3c97b6bf7e29dbe173e84d3ff56380823`  
		Last Modified: Tue, 21 Oct 2025 04:34:25 GMT  
		Size: 11.7 MB (11659902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27929b078986502b92d9386cf999508c186d976502094d31f9422209b7a3f459`  
		Last Modified: Tue, 21 Oct 2025 04:34:32 GMT  
		Size: 127.4 MB (127368126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879dbe16d2cc622be175350d82500f51f0c4cc0229b9f053c06df5f9e14be9c`  
		Last Modified: Tue, 21 Oct 2025 04:34:24 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:b995f50fb036806a6c149022b0542072ca38052d26b9431b53b0ff8e4d8e5b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5586422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21b6af0016282deb192da392c34d6668bf33eb2ccd7608019742163ef55a4`

```dockerfile
```

-	Layers:
	-	`sha256:b744f421054207dcfbfc26d2fa8b433cc2cad21922b9aea6d35cc72bc7537d62`  
		Last Modified: Tue, 21 Oct 2025 09:45:54 GMT  
		Size: 5.6 MB (5556730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359ef7cf0f362e274b5fdfce92bc56999680b403e589829b86579be6ad1e01bc`  
		Last Modified: Tue, 21 Oct 2025 09:45:55 GMT  
		Size: 29.7 KB (29692 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c47af56f42eb7a653433e87b4fb222c45558abd3a40c99702ed9ad7c9ac9104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218617983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e21c6c89aaad2f667bf50f8b18d9edf7ed7037fc2c817a40fc057f7afc9386c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6efb3d89d6fbb561172dac0bac32b6471b483864b886fe2c368f1067cdababc`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85423f326066e5b8f27da57b383099ab376e8c4a5aef811c6c3585a6c5408c51`  
		Last Modified: Tue, 21 Oct 2025 01:53:29 GMT  
		Size: 49.5 MB (49527078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be39782492fdb1e331910941d37268b079b5c40902a14bf080c011304f93678`  
		Last Modified: Tue, 21 Oct 2025 01:53:26 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bbe160aa659a28e1734f2db7b579f339cfe1318b77d8224d726a60791087ef`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4ed615b323eed16b6eababfc34f00f2bd476d3ecc22dbe6c75b83316652e5`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 1.2 MB (1201368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561bc5c5a5ab4d1e1cf0e6b9ba23ae99b562ced5698d734cc78e86b06a589c4d`  
		Last Modified: Tue, 21 Oct 2025 02:55:29 GMT  
		Size: 11.7 MB (11664635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed1a2ab1ec332f0e972d6a60f41970f9741b0118134a4e9260cd616e2afb25`  
		Last Modified: Tue, 21 Oct 2025 02:55:42 GMT  
		Size: 126.4 MB (126405759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ef1ca878c2a6c23796070519927497295064b3716fbb5c6a2f9818a01bd9e1`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:0c93fac739fe60f4f72635709e82f3c45ad9a864286dcab9c93d0a4464b53bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dc578c7ea8fcef555fe487fddf696c722448d11b02cd58ea682a2a49f84a30`

```dockerfile
```

-	Layers:
	-	`sha256:312b73581d5cf7220f576a145f5e58ed1f134653d0a349fcc99f6702cd06ed42`  
		Last Modified: Tue, 21 Oct 2025 09:46:00 GMT  
		Size: 5.6 MB (5554266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cda9550065f120bf2273bb59be7890c430bc005bdf298e0271670e357e792f`  
		Last Modified: Tue, 21 Oct 2025 09:46:01 GMT  
		Size: 29.7 KB (29720 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; ppc64le

```console
$ docker pull ghost@sha256:12c318536387a510d4778defab8940dbc4a0c3b4cafb2c9ad1c24566d0948085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229242707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2681de0a58f99ad4817eacfe98c0be6d2ebd096fa024f3c0985c5fae6f2139a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9450cb0ad48e77b8c7761b8d7fa9475ff419eb4a608d4f32cd964f9a72670`  
		Last Modified: Tue, 30 Sep 2025 02:48:33 GMT  
		Size: 52.3 MB (52337574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6b4d67e724f98a40f227d607e8b19f8c022311f853dff99d21082838be5cc`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 1.7 MB (1712763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99f21b04f5204e1b4372936a87d3f5c9b6e17b55765bcba9cc5e26c8516a33e`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e8ae3158969af71841027c5c4fb9383637b9a508b42c1ed4dfc98ac4e5d47`  
		Last Modified: Thu, 09 Oct 2025 18:34:34 GMT  
		Size: 1.2 MB (1206289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847f4b8f0e3e298ced64127f395fedfeaec0be21be8d9ddb828f1ad0bb0177`  
		Last Modified: Thu, 09 Oct 2025 18:34:36 GMT  
		Size: 11.7 MB (11656635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cce27bc0d5228a740cb51459bcdf46a0432a4edb389f7e28e452a0a47ea568`  
		Last Modified: Sat, 18 Oct 2025 12:01:37 GMT  
		Size: 130.3 MB (130256418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e27719d9e048ccb9e7d727c637b7da293c04d8fa10f43aec70311461877a671`  
		Last Modified: Sat, 18 Oct 2025 00:34:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:88ba8763237f9d0f1c30c4877c64c2d16731eddb12be1b20b07878e9b14e9b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5582663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726272f6f5390fa97e3283252b511318d9f20138a88ea678591f49293c2d2c8`

```dockerfile
```

-	Layers:
	-	`sha256:8b5e7e918af2e24e3268578ef18f68bf9454d19aa8d65bb79199a1209d48f26c`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 5.6 MB (5553029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b58d9d49d4fe0d4fbb6e80a147e65e90d9ebecb4bb1c865116509751d258c4`  
		Last Modified: Sat, 18 Oct 2025 03:45:53 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:afd7a11b44a684e29f7e4a35f951b562bb2d2130a65b46d06bfc7dca267d9233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220526578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d0fdb3c1d0f3ac8a2089f6ec012b219cca0a5abb2c01f9b3df625b14784d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1ef775861addedb3c47f18021d9a8fbdf772f8cd1d622722de95d54eed3c8f`  
		Last Modified: Tue, 30 Sep 2025 03:31:27 GMT  
		Size: 49.6 MB (49590828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67806ce7ef92e8d06544d92ebc309872ff6c32287bff4cb5a9664962e95a359`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2bfded38c5ae1160660e490c3743aae01c21ea3b80049ceca9825514a964cf`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f6c1312c799b5711fa348eb696800f3947f641f37d80109b438cc3fcf5835`  
		Last Modified: Thu, 09 Oct 2025 18:56:28 GMT  
		Size: 1.2 MB (1221134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fea8d7ebe3962eded038f9c7f2c02df3bffd9b603d05cc54f25e4a5e5c72585`  
		Last Modified: Thu, 09 Oct 2025 18:56:29 GMT  
		Size: 11.7 MB (11667690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f66e9132158eff2abb1b4642609b348ad0a4a0734dad97ae6c83ac2ca886b4`  
		Last Modified: Sat, 18 Oct 2025 18:42:04 GMT  
		Size: 129.4 MB (129445694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3502cf0d044992d10453795fc317fc6f47b69c6cef8875b704a1eaec767d5f88`  
		Last Modified: Sat, 18 Oct 2025 00:30:18 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:918cd556a5732d3b8ddcb2b8001a1f4590e944350b88c80efc50706a2580afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5576585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0a94915b1692e192f20275994e574c3c1c18964796d51cf1940f1101d2d054`

```dockerfile
```

-	Layers:
	-	`sha256:633bce997aedcc74f5037b7b76886fe32ce9beadd8c0eebe7cd0d34066c43963`  
		Last Modified: Sat, 18 Oct 2025 03:45:57 GMT  
		Size: 5.5 MB (5546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459a34e959e8ab2a3e782ba19bffb9b62bccc7f8e8273b14bdbd779fbdb271aa`  
		Last Modified: Sat, 18 Oct 2025 03:45:58 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:8a72ec9676734569570538838cbda1ab2389578f68870eede3a018da83b3e7c1
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
$ docker pull ghost@sha256:12fbffc2e0df73204d397cca5ae44797be54f9991adca2671e151c450f2d6dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196013578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8b24d4ecd61186acfbeb1f28494dde035ca25fe041a9ed80b30def9504ff49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f385331c129e26191cd1be348031f074d5cef6ae65f0b4c575f5470aeeb5290`  
		Last Modified: Wed, 08 Oct 2025 23:11:39 GMT  
		Size: 51.5 MB (51485406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd7e47c1da3b1d6d5752f0fe515ebf93bef68421b4748c48302b6b6dddc0dc`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a43d49c5117bb6048f44499d8980962eb8c429b52ea12441d635c0c1c9a56b`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb69ac78192fce08b521a9df89e18a8f7dc3a9105c50d1cc1189db1ff27c1f5`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724ae68776b49caf3e12ac9d58d9402838cd3358e364b273b9ac05c5d40f14c`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 923.4 KB (923438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275b74970cb03c16331b016cd9939853b452f87372a86a4c40389b9c5be79036`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a25555d57ab3539ed771059c8521185b7ae6e80269f40f7c99f44b4d6951813`  
		Last Modified: Sat, 18 Oct 2025 00:29:20 GMT  
		Size: 11.7 MB (11657533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2362a39ea89169422cc185eb74c06b004d0dcedcb661947bf6b5fada1eec3b`  
		Last Modified: Sat, 18 Oct 2025 00:29:34 GMT  
		Size: 126.1 MB (126105923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba44311e3a69dfbf4bff73b14ec2e632021b964655cd313edb9dd67c3dbe287`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:02ae8eed66e146e5089f0b50e26900486150bed19c3b4ab916bfeeaeb02a9ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bffc43a9839864e7bbdf5a53b4fe85c6a51d22dd02630977801f7a9cfe94a40`

```dockerfile
```

-	Layers:
	-	`sha256:212e7e2ed7c9bf01d71763f91c84af92f9a7fdcc3be9cb21487e49dd147df03c`  
		Last Modified: Sat, 18 Oct 2025 03:45:51 GMT  
		Size: 3.3 MB (3340058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96566977bfe6f9660e00f242377960d0344565ccc624d780087c19d7aad1ea4e`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 32.6 KB (32554 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:e5d0f670d32e199f3716c2217f4cdd5d30ebbfb1fe878da07e36954a4ebd111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194740738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cce56a6f76c32dbcc85190738a1fbbe2f5e28f86d326208f5bde14dfa67ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bdd99e34712933a46f4c5e673752ba0902911086ef21b0fd05e75298983d0`  
		Last Modified: Wed, 08 Oct 2025 23:36:42 GMT  
		Size: 49.2 MB (49171450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413aa9ff83db8d823557459e1067061c28ec022d0903e0c8d585379b803368f2`  
		Last Modified: Wed, 08 Oct 2025 23:24:04 GMT  
		Size: 1.3 MB (1260561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515a3451535d72e062ce7b4ad2ec3061d8237bac9325d48cf6640b9b2bfb9c6`  
		Last Modified: Wed, 08 Oct 2025 23:24:08 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d54d0234216e5ee50b6c50ad8fdbbc79a766aac6dd54f0f0dbae8b27e780b`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427c8ab41e6da116a5d6ceff26ea4fcc2bc67ebb3be6cf183c07fe6f5649569`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 889.1 KB (889104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2418b617ace496bf08e707ea72732efe91fd4f5db7bc647949dd2f1464db9`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13ceff8223b9c0da58baef50e8fe3ebc34e37ec8ccac45bd4ea8b8bbaa543ef`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 11.7 MB (11658915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192ca5aa7254be1abd81c4c13041176c295a950f1a915028e0d6170f1a680ac`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 127.5 MB (127489346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000fb46604660c74fd92f91a092c0be218483d49e4bb3574e591d56c8974a5f`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:615ebdb6f060e1d0e03f301922e3ecdc9671af9eabeac9d02e3374cefc787a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3b9d966f1fe5d4b5ddc2548b81e296d80ce15f4b2445b41b99ad0c543a484e`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c7cddcb6aa27438ac5bb9936bc52be204811ed7084452e04aa8c4774ab210`  
		Last Modified: Sat, 18 Oct 2025 03:45:56 GMT  
		Size: 32.5 KB (32471 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a9b07a213a28dfd4578d6c9d8dd06bf6f24a421e1fee28be39bcfe4c1c5cfb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced87ecaae4b043bb4783679034696a04c2737a6e00755ccd1cb7b9f0bbea4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bea9d721b81739ae5afd1f43120131a937526df8a6915bcc5e45623c9dc3b67`  
		Last Modified: Wed, 08 Oct 2025 23:53:57 GMT  
		Size: 48.5 MB (48468220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984624dfaf62780b5725d1309a1eb1c8cb1d14439d384d9a088b6855536569ac`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a0c86a699a44ef49e0e96f977a6d6c34b4ffaf0584fc92e46c0c8a7503bab`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f9110eb5d505dad4577030c2949259fd2773e8baaf4ad9da1c4d84e19dcf8`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 701.5 KB (701483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d87d3255e074041ee5f0a12b3c1ac2431419e9aeb052f6bbfa5782a278b6e`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 889.1 KB (889098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3483e2b8d336d6454583116a36d40c25fb8f7a16c958e9ec723d600d054e72`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb77968a89a9be12fa3fa96505d6b6d281b3bea7e4412ffa8a46d2028c32797`  
		Last Modified: Sat, 18 Oct 2025 00:31:43 GMT  
		Size: 11.7 MB (11651330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05980c28f231f956a3ed45f51a9d0b1aef67bf6cceff1a4359755619d3df298`  
		Last Modified: Sat, 18 Oct 2025 00:31:51 GMT  
		Size: 127.2 MB (127174816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c33eae9d972262247fc5c605723aa1186b38782cdf1e9d45ab4a019c09c269`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:336f27e6ea1cab5985ecfe2f1344d4ac0d33684c0dbd3acb27869511e850ed64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3369769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce55101537eca36370070a09e8e607e497917f5417e62bfda9dc1cf426e5d51`

```dockerfile
```

-	Layers:
	-	`sha256:aa2c0cfc7990958bb3a493fc455e7efcc5574f01b555329760327dbd2242544f`  
		Last Modified: Sat, 18 Oct 2025 03:45:59 GMT  
		Size: 3.3 MB (3337083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce534b3719e8f4ef66e95ec1b0974cf5871c9812dea861636656bcf361b4141`  
		Last Modified: Sat, 18 Oct 2025 03:46:00 GMT  
		Size: 32.7 KB (32686 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:98912b55682059cceb54c93973a7f25bb0eec4547b79b26176da014337cfeab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206874888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36db5a036f2c1e2cb52ed89b18108b95198dc7b64e07b8dc599a2aa908b0b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d61e981703581f111feeaf3584550c7b2b22ac5c57a260d76386576bad8c438`  
		Last Modified: Wed, 08 Oct 2025 22:44:22 GMT  
		Size: 51.2 MB (51199404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6507169272064be83968b71a12bac1a223eb06cffa85615ce0ad229fc6bc54`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846561b46d4c3d9791e970078963c3be4ce306bc370156b98f8182e8079f5`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8b4df016b28cd75d4087813cbce98ed88e94e31dc2e4af61c30d20ef5d7f1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 838.6 KB (838570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b95a0c3e08205cf3722856e1453d43185c5cfb3e62a928492082022ef8f89`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 876.4 KB (876366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ca8465c4106c99cc321da47509d129f031cfe8f765255226b8ae829204d5d1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3374586f03c6371486b749afe721e3d6a0892430d5f48d1b252f0ae845c746b7`  
		Last Modified: Sat, 18 Oct 2025 00:32:17 GMT  
		Size: 11.7 MB (11656937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6013f3a38fdf8e386e7e7359dbafff49de28d66f59f85d20b1dcb0f60c3d0fdf`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 136.9 MB (136903774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa87ec0ea679e4fe3e6426e246dc107584dc7e8b1f88d6ce8a074952bc3b7d8`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e08016234ab4d76c3bd758ff8687267d7d9f4708ae9129820d11b283b5933c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4788db0a4b56b72acdf053a5cc892e885dfafb70b9917282d44794258abcf63e`

```dockerfile
```

-	Layers:
	-	`sha256:e68121590c2a2a419a67d03d337e6d76f45dd11c961c091ff97e6a4f64d4293a`  
		Last Modified: Sat, 18 Oct 2025 03:46:03 GMT  
		Size: 3.3 MB (3340166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13969f68868d68b0bd533141c2264f7fc02d01055749ad77fa8d87b60b92872`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 32.7 KB (32718 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.4`

```console
$ docker pull ghost@sha256:7686d30f30383bb08df0dcd5c89fd897c4e2112d3f6a50f8ecdb78cf021bad2e
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

### `ghost:6.4` - linux; amd64

```console
$ docker pull ghost@sha256:e0d477eca26277b7868de615763a27a8d75724bebdc72f8e42ba716d7d5f133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218576394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c46db0139e218d0602cd5e87b8e96145de5fa8a722502670a1eac235387378f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98ba22ffba63e671e794151a8c72b2dd2e2394a99dfdadb48375658423035c`  
		Last Modified: Tue, 21 Oct 2025 01:49:16 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce3834b70636fccfd15681ae09efc245e61d942555ff1b60eff662498f71f8`  
		Last Modified: Tue, 21 Oct 2025 01:49:20 GMT  
		Size: 49.4 MB (49406240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4168ab2bca6183681fd3571770924ab57da32eadefdb46f2208e8d8e572011`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e85ddc713935ca5a0accf8aec281f24ed3e23d93f11df909657e9ee9a0403`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184228eff12de998e31c119c22628a0214103d642cb2565a8f3e8f63f443bb1`  
		Last Modified: Tue, 21 Oct 2025 05:05:15 GMT  
		Size: 1.2 MB (1247341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3edd59bde935bd9eb92e8a1d7062f172dff05ee19bd9154471d701aa16affd9`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 11.7 MB (11661483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46bdfee218799cc3f27d6745d89a93a4047bf50be50e3e2ee83cd465d74fc52`  
		Last Modified: Tue, 21 Oct 2025 05:05:23 GMT  
		Size: 126.3 MB (126316069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63b4f25f0e618fed546bcd79af50eaa4e82811670015b2e7e0a784fddb26d21`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4` - unknown; unknown

```console
$ docker pull ghost@sha256:6f4e0d84f80c4c7af9ea51d490fb0a102070b88740f56050d19d6d6cd3b9927e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4ac880fa060e58864e38bfa6a08c0084a3f01ca86672c61cdba47104730bf`

```dockerfile
```

-	Layers:
	-	`sha256:e7d16010c082e36f6352e043cc8ad362b86ee7ce147b43037b74ebbdf9e48814`  
		Last Modified: Tue, 21 Oct 2025 09:45:47 GMT  
		Size: 5.6 MB (5553963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0aa203325540398a2d4bb16fb5c221dc12e68ee0752c49dec8160b877b0c09`  
		Last Modified: Tue, 21 Oct 2025 09:45:48 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a8d79fc46cfa3b2146fa9fdd21dfb3b7268ba7494cd810b3ffe794d580823271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210030395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26bf23785bc61c442262280e3ac6923f91b3c3a6d757abe11c45c98aa1dae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b71629629a04cc6e17d182034fdc2181577adfa385f1edbfc4dd8bc3d17a38a`  
		Last Modified: Tue, 21 Oct 2025 02:57:36 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b787ce0420c13b5936470725c1246c0a56bb1980f368545047829b37396961`  
		Last Modified: Tue, 21 Oct 2025 02:57:38 GMT  
		Size: 44.1 MB (44136924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ab4cac8e6724a34f622a34a9016e857f8280ad0ec6152728226d371344e12`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 1.7 MB (1712852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e3d58d86740d69693dd91be91201911df44b63d9904f076ebe3cb30c5e100`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636d5fe8a91c198d3cec1a0f69391c7eddc5173ef352005fb1b98d5931561b7`  
		Last Modified: Tue, 21 Oct 2025 04:34:23 GMT  
		Size: 1.2 MB (1214242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12442508853d21a7948b51aeaac6c3c97b6bf7e29dbe173e84d3ff56380823`  
		Last Modified: Tue, 21 Oct 2025 04:34:25 GMT  
		Size: 11.7 MB (11659902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27929b078986502b92d9386cf999508c186d976502094d31f9422209b7a3f459`  
		Last Modified: Tue, 21 Oct 2025 04:34:32 GMT  
		Size: 127.4 MB (127368126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879dbe16d2cc622be175350d82500f51f0c4cc0229b9f053c06df5f9e14be9c`  
		Last Modified: Tue, 21 Oct 2025 04:34:24 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4` - unknown; unknown

```console
$ docker pull ghost@sha256:b995f50fb036806a6c149022b0542072ca38052d26b9431b53b0ff8e4d8e5b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5586422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21b6af0016282deb192da392c34d6668bf33eb2ccd7608019742163ef55a4`

```dockerfile
```

-	Layers:
	-	`sha256:b744f421054207dcfbfc26d2fa8b433cc2cad21922b9aea6d35cc72bc7537d62`  
		Last Modified: Tue, 21 Oct 2025 09:45:54 GMT  
		Size: 5.6 MB (5556730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359ef7cf0f362e274b5fdfce92bc56999680b403e589829b86579be6ad1e01bc`  
		Last Modified: Tue, 21 Oct 2025 09:45:55 GMT  
		Size: 29.7 KB (29692 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c47af56f42eb7a653433e87b4fb222c45558abd3a40c99702ed9ad7c9ac9104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218617983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e21c6c89aaad2f667bf50f8b18d9edf7ed7037fc2c817a40fc057f7afc9386c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6efb3d89d6fbb561172dac0bac32b6471b483864b886fe2c368f1067cdababc`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85423f326066e5b8f27da57b383099ab376e8c4a5aef811c6c3585a6c5408c51`  
		Last Modified: Tue, 21 Oct 2025 01:53:29 GMT  
		Size: 49.5 MB (49527078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be39782492fdb1e331910941d37268b079b5c40902a14bf080c011304f93678`  
		Last Modified: Tue, 21 Oct 2025 01:53:26 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bbe160aa659a28e1734f2db7b579f339cfe1318b77d8224d726a60791087ef`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4ed615b323eed16b6eababfc34f00f2bd476d3ecc22dbe6c75b83316652e5`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 1.2 MB (1201368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561bc5c5a5ab4d1e1cf0e6b9ba23ae99b562ced5698d734cc78e86b06a589c4d`  
		Last Modified: Tue, 21 Oct 2025 02:55:29 GMT  
		Size: 11.7 MB (11664635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed1a2ab1ec332f0e972d6a60f41970f9741b0118134a4e9260cd616e2afb25`  
		Last Modified: Tue, 21 Oct 2025 02:55:42 GMT  
		Size: 126.4 MB (126405759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ef1ca878c2a6c23796070519927497295064b3716fbb5c6a2f9818a01bd9e1`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4` - unknown; unknown

```console
$ docker pull ghost@sha256:0c93fac739fe60f4f72635709e82f3c45ad9a864286dcab9c93d0a4464b53bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dc578c7ea8fcef555fe487fddf696c722448d11b02cd58ea682a2a49f84a30`

```dockerfile
```

-	Layers:
	-	`sha256:312b73581d5cf7220f576a145f5e58ed1f134653d0a349fcc99f6702cd06ed42`  
		Last Modified: Tue, 21 Oct 2025 09:46:00 GMT  
		Size: 5.6 MB (5554266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cda9550065f120bf2273bb59be7890c430bc005bdf298e0271670e357e792f`  
		Last Modified: Tue, 21 Oct 2025 09:46:01 GMT  
		Size: 29.7 KB (29720 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4` - linux; ppc64le

```console
$ docker pull ghost@sha256:12c318536387a510d4778defab8940dbc4a0c3b4cafb2c9ad1c24566d0948085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229242707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2681de0a58f99ad4817eacfe98c0be6d2ebd096fa024f3c0985c5fae6f2139a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9450cb0ad48e77b8c7761b8d7fa9475ff419eb4a608d4f32cd964f9a72670`  
		Last Modified: Tue, 30 Sep 2025 02:48:33 GMT  
		Size: 52.3 MB (52337574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6b4d67e724f98a40f227d607e8b19f8c022311f853dff99d21082838be5cc`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 1.7 MB (1712763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99f21b04f5204e1b4372936a87d3f5c9b6e17b55765bcba9cc5e26c8516a33e`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e8ae3158969af71841027c5c4fb9383637b9a508b42c1ed4dfc98ac4e5d47`  
		Last Modified: Thu, 09 Oct 2025 18:34:34 GMT  
		Size: 1.2 MB (1206289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847f4b8f0e3e298ced64127f395fedfeaec0be21be8d9ddb828f1ad0bb0177`  
		Last Modified: Thu, 09 Oct 2025 18:34:36 GMT  
		Size: 11.7 MB (11656635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cce27bc0d5228a740cb51459bcdf46a0432a4edb389f7e28e452a0a47ea568`  
		Last Modified: Sat, 18 Oct 2025 12:01:37 GMT  
		Size: 130.3 MB (130256418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e27719d9e048ccb9e7d727c637b7da293c04d8fa10f43aec70311461877a671`  
		Last Modified: Sat, 18 Oct 2025 00:34:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4` - unknown; unknown

```console
$ docker pull ghost@sha256:88ba8763237f9d0f1c30c4877c64c2d16731eddb12be1b20b07878e9b14e9b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5582663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726272f6f5390fa97e3283252b511318d9f20138a88ea678591f49293c2d2c8`

```dockerfile
```

-	Layers:
	-	`sha256:8b5e7e918af2e24e3268578ef18f68bf9454d19aa8d65bb79199a1209d48f26c`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 5.6 MB (5553029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b58d9d49d4fe0d4fbb6e80a147e65e90d9ebecb4bb1c865116509751d258c4`  
		Last Modified: Sat, 18 Oct 2025 03:45:53 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4` - linux; s390x

```console
$ docker pull ghost@sha256:afd7a11b44a684e29f7e4a35f951b562bb2d2130a65b46d06bfc7dca267d9233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220526578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d0fdb3c1d0f3ac8a2089f6ec012b219cca0a5abb2c01f9b3df625b14784d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1ef775861addedb3c47f18021d9a8fbdf772f8cd1d622722de95d54eed3c8f`  
		Last Modified: Tue, 30 Sep 2025 03:31:27 GMT  
		Size: 49.6 MB (49590828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67806ce7ef92e8d06544d92ebc309872ff6c32287bff4cb5a9664962e95a359`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2bfded38c5ae1160660e490c3743aae01c21ea3b80049ceca9825514a964cf`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f6c1312c799b5711fa348eb696800f3947f641f37d80109b438cc3fcf5835`  
		Last Modified: Thu, 09 Oct 2025 18:56:28 GMT  
		Size: 1.2 MB (1221134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fea8d7ebe3962eded038f9c7f2c02df3bffd9b603d05cc54f25e4a5e5c72585`  
		Last Modified: Thu, 09 Oct 2025 18:56:29 GMT  
		Size: 11.7 MB (11667690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f66e9132158eff2abb1b4642609b348ad0a4a0734dad97ae6c83ac2ca886b4`  
		Last Modified: Sat, 18 Oct 2025 18:42:04 GMT  
		Size: 129.4 MB (129445694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3502cf0d044992d10453795fc317fc6f47b69c6cef8875b704a1eaec767d5f88`  
		Last Modified: Sat, 18 Oct 2025 00:30:18 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4` - unknown; unknown

```console
$ docker pull ghost@sha256:918cd556a5732d3b8ddcb2b8001a1f4590e944350b88c80efc50706a2580afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5576585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0a94915b1692e192f20275994e574c3c1c18964796d51cf1940f1101d2d054`

```dockerfile
```

-	Layers:
	-	`sha256:633bce997aedcc74f5037b7b76886fe32ce9beadd8c0eebe7cd0d34066c43963`  
		Last Modified: Sat, 18 Oct 2025 03:45:57 GMT  
		Size: 5.5 MB (5546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459a34e959e8ab2a3e782ba19bffb9b62bccc7f8e8273b14bdbd779fbdb271aa`  
		Last Modified: Sat, 18 Oct 2025 03:45:58 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.4-alpine`

```console
$ docker pull ghost@sha256:8a72ec9676734569570538838cbda1ab2389578f68870eede3a018da83b3e7c1
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

### `ghost:6.4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:12fbffc2e0df73204d397cca5ae44797be54f9991adca2671e151c450f2d6dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196013578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8b24d4ecd61186acfbeb1f28494dde035ca25fe041a9ed80b30def9504ff49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f385331c129e26191cd1be348031f074d5cef6ae65f0b4c575f5470aeeb5290`  
		Last Modified: Wed, 08 Oct 2025 23:11:39 GMT  
		Size: 51.5 MB (51485406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd7e47c1da3b1d6d5752f0fe515ebf93bef68421b4748c48302b6b6dddc0dc`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a43d49c5117bb6048f44499d8980962eb8c429b52ea12441d635c0c1c9a56b`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb69ac78192fce08b521a9df89e18a8f7dc3a9105c50d1cc1189db1ff27c1f5`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724ae68776b49caf3e12ac9d58d9402838cd3358e364b273b9ac05c5d40f14c`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 923.4 KB (923438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275b74970cb03c16331b016cd9939853b452f87372a86a4c40389b9c5be79036`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a25555d57ab3539ed771059c8521185b7ae6e80269f40f7c99f44b4d6951813`  
		Last Modified: Sat, 18 Oct 2025 00:29:20 GMT  
		Size: 11.7 MB (11657533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2362a39ea89169422cc185eb74c06b004d0dcedcb661947bf6b5fada1eec3b`  
		Last Modified: Sat, 18 Oct 2025 00:29:34 GMT  
		Size: 126.1 MB (126105923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba44311e3a69dfbf4bff73b14ec2e632021b964655cd313edb9dd67c3dbe287`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:02ae8eed66e146e5089f0b50e26900486150bed19c3b4ab916bfeeaeb02a9ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bffc43a9839864e7bbdf5a53b4fe85c6a51d22dd02630977801f7a9cfe94a40`

```dockerfile
```

-	Layers:
	-	`sha256:212e7e2ed7c9bf01d71763f91c84af92f9a7fdcc3be9cb21487e49dd147df03c`  
		Last Modified: Sat, 18 Oct 2025 03:45:51 GMT  
		Size: 3.3 MB (3340058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96566977bfe6f9660e00f242377960d0344565ccc624d780087c19d7aad1ea4e`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 32.6 KB (32554 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:e5d0f670d32e199f3716c2217f4cdd5d30ebbfb1fe878da07e36954a4ebd111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194740738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cce56a6f76c32dbcc85190738a1fbbe2f5e28f86d326208f5bde14dfa67ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bdd99e34712933a46f4c5e673752ba0902911086ef21b0fd05e75298983d0`  
		Last Modified: Wed, 08 Oct 2025 23:36:42 GMT  
		Size: 49.2 MB (49171450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413aa9ff83db8d823557459e1067061c28ec022d0903e0c8d585379b803368f2`  
		Last Modified: Wed, 08 Oct 2025 23:24:04 GMT  
		Size: 1.3 MB (1260561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515a3451535d72e062ce7b4ad2ec3061d8237bac9325d48cf6640b9b2bfb9c6`  
		Last Modified: Wed, 08 Oct 2025 23:24:08 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d54d0234216e5ee50b6c50ad8fdbbc79a766aac6dd54f0f0dbae8b27e780b`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427c8ab41e6da116a5d6ceff26ea4fcc2bc67ebb3be6cf183c07fe6f5649569`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 889.1 KB (889104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2418b617ace496bf08e707ea72732efe91fd4f5db7bc647949dd2f1464db9`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13ceff8223b9c0da58baef50e8fe3ebc34e37ec8ccac45bd4ea8b8bbaa543ef`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 11.7 MB (11658915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192ca5aa7254be1abd81c4c13041176c295a950f1a915028e0d6170f1a680ac`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 127.5 MB (127489346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000fb46604660c74fd92f91a092c0be218483d49e4bb3574e591d56c8974a5f`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:615ebdb6f060e1d0e03f301922e3ecdc9671af9eabeac9d02e3374cefc787a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3b9d966f1fe5d4b5ddc2548b81e296d80ce15f4b2445b41b99ad0c543a484e`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c7cddcb6aa27438ac5bb9936bc52be204811ed7084452e04aa8c4774ab210`  
		Last Modified: Sat, 18 Oct 2025 03:45:56 GMT  
		Size: 32.5 KB (32471 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a9b07a213a28dfd4578d6c9d8dd06bf6f24a421e1fee28be39bcfe4c1c5cfb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced87ecaae4b043bb4783679034696a04c2737a6e00755ccd1cb7b9f0bbea4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bea9d721b81739ae5afd1f43120131a937526df8a6915bcc5e45623c9dc3b67`  
		Last Modified: Wed, 08 Oct 2025 23:53:57 GMT  
		Size: 48.5 MB (48468220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984624dfaf62780b5725d1309a1eb1c8cb1d14439d384d9a088b6855536569ac`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a0c86a699a44ef49e0e96f977a6d6c34b4ffaf0584fc92e46c0c8a7503bab`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f9110eb5d505dad4577030c2949259fd2773e8baaf4ad9da1c4d84e19dcf8`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 701.5 KB (701483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d87d3255e074041ee5f0a12b3c1ac2431419e9aeb052f6bbfa5782a278b6e`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 889.1 KB (889098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3483e2b8d336d6454583116a36d40c25fb8f7a16c958e9ec723d600d054e72`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb77968a89a9be12fa3fa96505d6b6d281b3bea7e4412ffa8a46d2028c32797`  
		Last Modified: Sat, 18 Oct 2025 00:31:43 GMT  
		Size: 11.7 MB (11651330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05980c28f231f956a3ed45f51a9d0b1aef67bf6cceff1a4359755619d3df298`  
		Last Modified: Sat, 18 Oct 2025 00:31:51 GMT  
		Size: 127.2 MB (127174816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c33eae9d972262247fc5c605723aa1186b38782cdf1e9d45ab4a019c09c269`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:336f27e6ea1cab5985ecfe2f1344d4ac0d33684c0dbd3acb27869511e850ed64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3369769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce55101537eca36370070a09e8e607e497917f5417e62bfda9dc1cf426e5d51`

```dockerfile
```

-	Layers:
	-	`sha256:aa2c0cfc7990958bb3a493fc455e7efcc5574f01b555329760327dbd2242544f`  
		Last Modified: Sat, 18 Oct 2025 03:45:59 GMT  
		Size: 3.3 MB (3337083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce534b3719e8f4ef66e95ec1b0974cf5871c9812dea861636656bcf361b4141`  
		Last Modified: Sat, 18 Oct 2025 03:46:00 GMT  
		Size: 32.7 KB (32686 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:98912b55682059cceb54c93973a7f25bb0eec4547b79b26176da014337cfeab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206874888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36db5a036f2c1e2cb52ed89b18108b95198dc7b64e07b8dc599a2aa908b0b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d61e981703581f111feeaf3584550c7b2b22ac5c57a260d76386576bad8c438`  
		Last Modified: Wed, 08 Oct 2025 22:44:22 GMT  
		Size: 51.2 MB (51199404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6507169272064be83968b71a12bac1a223eb06cffa85615ce0ad229fc6bc54`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846561b46d4c3d9791e970078963c3be4ce306bc370156b98f8182e8079f5`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8b4df016b28cd75d4087813cbce98ed88e94e31dc2e4af61c30d20ef5d7f1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 838.6 KB (838570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b95a0c3e08205cf3722856e1453d43185c5cfb3e62a928492082022ef8f89`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 876.4 KB (876366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ca8465c4106c99cc321da47509d129f031cfe8f765255226b8ae829204d5d1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3374586f03c6371486b749afe721e3d6a0892430d5f48d1b252f0ae845c746b7`  
		Last Modified: Sat, 18 Oct 2025 00:32:17 GMT  
		Size: 11.7 MB (11656937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6013f3a38fdf8e386e7e7359dbafff49de28d66f59f85d20b1dcb0f60c3d0fdf`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 136.9 MB (136903774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa87ec0ea679e4fe3e6426e246dc107584dc7e8b1f88d6ce8a074952bc3b7d8`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e08016234ab4d76c3bd758ff8687267d7d9f4708ae9129820d11b283b5933c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4788db0a4b56b72acdf053a5cc892e885dfafb70b9917282d44794258abcf63e`

```dockerfile
```

-	Layers:
	-	`sha256:e68121590c2a2a419a67d03d337e6d76f45dd11c961c091ff97e6a4f64d4293a`  
		Last Modified: Sat, 18 Oct 2025 03:46:03 GMT  
		Size: 3.3 MB (3340166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13969f68868d68b0bd533141c2264f7fc02d01055749ad77fa8d87b60b92872`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 32.7 KB (32718 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.4.0`

```console
$ docker pull ghost@sha256:7686d30f30383bb08df0dcd5c89fd897c4e2112d3f6a50f8ecdb78cf021bad2e
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

### `ghost:6.4.0` - linux; amd64

```console
$ docker pull ghost@sha256:e0d477eca26277b7868de615763a27a8d75724bebdc72f8e42ba716d7d5f133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218576394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c46db0139e218d0602cd5e87b8e96145de5fa8a722502670a1eac235387378f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98ba22ffba63e671e794151a8c72b2dd2e2394a99dfdadb48375658423035c`  
		Last Modified: Tue, 21 Oct 2025 01:49:16 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce3834b70636fccfd15681ae09efc245e61d942555ff1b60eff662498f71f8`  
		Last Modified: Tue, 21 Oct 2025 01:49:20 GMT  
		Size: 49.4 MB (49406240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4168ab2bca6183681fd3571770924ab57da32eadefdb46f2208e8d8e572011`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e85ddc713935ca5a0accf8aec281f24ed3e23d93f11df909657e9ee9a0403`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184228eff12de998e31c119c22628a0214103d642cb2565a8f3e8f63f443bb1`  
		Last Modified: Tue, 21 Oct 2025 05:05:15 GMT  
		Size: 1.2 MB (1247341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3edd59bde935bd9eb92e8a1d7062f172dff05ee19bd9154471d701aa16affd9`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 11.7 MB (11661483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46bdfee218799cc3f27d6745d89a93a4047bf50be50e3e2ee83cd465d74fc52`  
		Last Modified: Tue, 21 Oct 2025 05:05:23 GMT  
		Size: 126.3 MB (126316069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63b4f25f0e618fed546bcd79af50eaa4e82811670015b2e7e0a784fddb26d21`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0` - unknown; unknown

```console
$ docker pull ghost@sha256:6f4e0d84f80c4c7af9ea51d490fb0a102070b88740f56050d19d6d6cd3b9927e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4ac880fa060e58864e38bfa6a08c0084a3f01ca86672c61cdba47104730bf`

```dockerfile
```

-	Layers:
	-	`sha256:e7d16010c082e36f6352e043cc8ad362b86ee7ce147b43037b74ebbdf9e48814`  
		Last Modified: Tue, 21 Oct 2025 09:45:47 GMT  
		Size: 5.6 MB (5553963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0aa203325540398a2d4bb16fb5c221dc12e68ee0752c49dec8160b877b0c09`  
		Last Modified: Tue, 21 Oct 2025 09:45:48 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a8d79fc46cfa3b2146fa9fdd21dfb3b7268ba7494cd810b3ffe794d580823271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210030395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26bf23785bc61c442262280e3ac6923f91b3c3a6d757abe11c45c98aa1dae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b71629629a04cc6e17d182034fdc2181577adfa385f1edbfc4dd8bc3d17a38a`  
		Last Modified: Tue, 21 Oct 2025 02:57:36 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b787ce0420c13b5936470725c1246c0a56bb1980f368545047829b37396961`  
		Last Modified: Tue, 21 Oct 2025 02:57:38 GMT  
		Size: 44.1 MB (44136924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ab4cac8e6724a34f622a34a9016e857f8280ad0ec6152728226d371344e12`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 1.7 MB (1712852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e3d58d86740d69693dd91be91201911df44b63d9904f076ebe3cb30c5e100`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636d5fe8a91c198d3cec1a0f69391c7eddc5173ef352005fb1b98d5931561b7`  
		Last Modified: Tue, 21 Oct 2025 04:34:23 GMT  
		Size: 1.2 MB (1214242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12442508853d21a7948b51aeaac6c3c97b6bf7e29dbe173e84d3ff56380823`  
		Last Modified: Tue, 21 Oct 2025 04:34:25 GMT  
		Size: 11.7 MB (11659902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27929b078986502b92d9386cf999508c186d976502094d31f9422209b7a3f459`  
		Last Modified: Tue, 21 Oct 2025 04:34:32 GMT  
		Size: 127.4 MB (127368126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879dbe16d2cc622be175350d82500f51f0c4cc0229b9f053c06df5f9e14be9c`  
		Last Modified: Tue, 21 Oct 2025 04:34:24 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0` - unknown; unknown

```console
$ docker pull ghost@sha256:b995f50fb036806a6c149022b0542072ca38052d26b9431b53b0ff8e4d8e5b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5586422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21b6af0016282deb192da392c34d6668bf33eb2ccd7608019742163ef55a4`

```dockerfile
```

-	Layers:
	-	`sha256:b744f421054207dcfbfc26d2fa8b433cc2cad21922b9aea6d35cc72bc7537d62`  
		Last Modified: Tue, 21 Oct 2025 09:45:54 GMT  
		Size: 5.6 MB (5556730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359ef7cf0f362e274b5fdfce92bc56999680b403e589829b86579be6ad1e01bc`  
		Last Modified: Tue, 21 Oct 2025 09:45:55 GMT  
		Size: 29.7 KB (29692 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c47af56f42eb7a653433e87b4fb222c45558abd3a40c99702ed9ad7c9ac9104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218617983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e21c6c89aaad2f667bf50f8b18d9edf7ed7037fc2c817a40fc057f7afc9386c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6efb3d89d6fbb561172dac0bac32b6471b483864b886fe2c368f1067cdababc`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85423f326066e5b8f27da57b383099ab376e8c4a5aef811c6c3585a6c5408c51`  
		Last Modified: Tue, 21 Oct 2025 01:53:29 GMT  
		Size: 49.5 MB (49527078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be39782492fdb1e331910941d37268b079b5c40902a14bf080c011304f93678`  
		Last Modified: Tue, 21 Oct 2025 01:53:26 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bbe160aa659a28e1734f2db7b579f339cfe1318b77d8224d726a60791087ef`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4ed615b323eed16b6eababfc34f00f2bd476d3ecc22dbe6c75b83316652e5`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 1.2 MB (1201368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561bc5c5a5ab4d1e1cf0e6b9ba23ae99b562ced5698d734cc78e86b06a589c4d`  
		Last Modified: Tue, 21 Oct 2025 02:55:29 GMT  
		Size: 11.7 MB (11664635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed1a2ab1ec332f0e972d6a60f41970f9741b0118134a4e9260cd616e2afb25`  
		Last Modified: Tue, 21 Oct 2025 02:55:42 GMT  
		Size: 126.4 MB (126405759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ef1ca878c2a6c23796070519927497295064b3716fbb5c6a2f9818a01bd9e1`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0` - unknown; unknown

```console
$ docker pull ghost@sha256:0c93fac739fe60f4f72635709e82f3c45ad9a864286dcab9c93d0a4464b53bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dc578c7ea8fcef555fe487fddf696c722448d11b02cd58ea682a2a49f84a30`

```dockerfile
```

-	Layers:
	-	`sha256:312b73581d5cf7220f576a145f5e58ed1f134653d0a349fcc99f6702cd06ed42`  
		Last Modified: Tue, 21 Oct 2025 09:46:00 GMT  
		Size: 5.6 MB (5554266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cda9550065f120bf2273bb59be7890c430bc005bdf298e0271670e357e792f`  
		Last Modified: Tue, 21 Oct 2025 09:46:01 GMT  
		Size: 29.7 KB (29720 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:12c318536387a510d4778defab8940dbc4a0c3b4cafb2c9ad1c24566d0948085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229242707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2681de0a58f99ad4817eacfe98c0be6d2ebd096fa024f3c0985c5fae6f2139a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9450cb0ad48e77b8c7761b8d7fa9475ff419eb4a608d4f32cd964f9a72670`  
		Last Modified: Tue, 30 Sep 2025 02:48:33 GMT  
		Size: 52.3 MB (52337574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6b4d67e724f98a40f227d607e8b19f8c022311f853dff99d21082838be5cc`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 1.7 MB (1712763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99f21b04f5204e1b4372936a87d3f5c9b6e17b55765bcba9cc5e26c8516a33e`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e8ae3158969af71841027c5c4fb9383637b9a508b42c1ed4dfc98ac4e5d47`  
		Last Modified: Thu, 09 Oct 2025 18:34:34 GMT  
		Size: 1.2 MB (1206289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847f4b8f0e3e298ced64127f395fedfeaec0be21be8d9ddb828f1ad0bb0177`  
		Last Modified: Thu, 09 Oct 2025 18:34:36 GMT  
		Size: 11.7 MB (11656635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cce27bc0d5228a740cb51459bcdf46a0432a4edb389f7e28e452a0a47ea568`  
		Last Modified: Sat, 18 Oct 2025 12:01:37 GMT  
		Size: 130.3 MB (130256418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e27719d9e048ccb9e7d727c637b7da293c04d8fa10f43aec70311461877a671`  
		Last Modified: Sat, 18 Oct 2025 00:34:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0` - unknown; unknown

```console
$ docker pull ghost@sha256:88ba8763237f9d0f1c30c4877c64c2d16731eddb12be1b20b07878e9b14e9b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5582663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726272f6f5390fa97e3283252b511318d9f20138a88ea678591f49293c2d2c8`

```dockerfile
```

-	Layers:
	-	`sha256:8b5e7e918af2e24e3268578ef18f68bf9454d19aa8d65bb79199a1209d48f26c`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 5.6 MB (5553029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b58d9d49d4fe0d4fbb6e80a147e65e90d9ebecb4bb1c865116509751d258c4`  
		Last Modified: Sat, 18 Oct 2025 03:45:53 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0` - linux; s390x

```console
$ docker pull ghost@sha256:afd7a11b44a684e29f7e4a35f951b562bb2d2130a65b46d06bfc7dca267d9233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220526578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d0fdb3c1d0f3ac8a2089f6ec012b219cca0a5abb2c01f9b3df625b14784d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1ef775861addedb3c47f18021d9a8fbdf772f8cd1d622722de95d54eed3c8f`  
		Last Modified: Tue, 30 Sep 2025 03:31:27 GMT  
		Size: 49.6 MB (49590828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67806ce7ef92e8d06544d92ebc309872ff6c32287bff4cb5a9664962e95a359`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2bfded38c5ae1160660e490c3743aae01c21ea3b80049ceca9825514a964cf`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f6c1312c799b5711fa348eb696800f3947f641f37d80109b438cc3fcf5835`  
		Last Modified: Thu, 09 Oct 2025 18:56:28 GMT  
		Size: 1.2 MB (1221134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fea8d7ebe3962eded038f9c7f2c02df3bffd9b603d05cc54f25e4a5e5c72585`  
		Last Modified: Thu, 09 Oct 2025 18:56:29 GMT  
		Size: 11.7 MB (11667690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f66e9132158eff2abb1b4642609b348ad0a4a0734dad97ae6c83ac2ca886b4`  
		Last Modified: Sat, 18 Oct 2025 18:42:04 GMT  
		Size: 129.4 MB (129445694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3502cf0d044992d10453795fc317fc6f47b69c6cef8875b704a1eaec767d5f88`  
		Last Modified: Sat, 18 Oct 2025 00:30:18 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0` - unknown; unknown

```console
$ docker pull ghost@sha256:918cd556a5732d3b8ddcb2b8001a1f4590e944350b88c80efc50706a2580afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5576585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0a94915b1692e192f20275994e574c3c1c18964796d51cf1940f1101d2d054`

```dockerfile
```

-	Layers:
	-	`sha256:633bce997aedcc74f5037b7b76886fe32ce9beadd8c0eebe7cd0d34066c43963`  
		Last Modified: Sat, 18 Oct 2025 03:45:57 GMT  
		Size: 5.5 MB (5546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459a34e959e8ab2a3e782ba19bffb9b62bccc7f8e8273b14bdbd779fbdb271aa`  
		Last Modified: Sat, 18 Oct 2025 03:45:58 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.4.0-alpine`

```console
$ docker pull ghost@sha256:8a72ec9676734569570538838cbda1ab2389578f68870eede3a018da83b3e7c1
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

### `ghost:6.4.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:12fbffc2e0df73204d397cca5ae44797be54f9991adca2671e151c450f2d6dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196013578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8b24d4ecd61186acfbeb1f28494dde035ca25fe041a9ed80b30def9504ff49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f385331c129e26191cd1be348031f074d5cef6ae65f0b4c575f5470aeeb5290`  
		Last Modified: Wed, 08 Oct 2025 23:11:39 GMT  
		Size: 51.5 MB (51485406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd7e47c1da3b1d6d5752f0fe515ebf93bef68421b4748c48302b6b6dddc0dc`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a43d49c5117bb6048f44499d8980962eb8c429b52ea12441d635c0c1c9a56b`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb69ac78192fce08b521a9df89e18a8f7dc3a9105c50d1cc1189db1ff27c1f5`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724ae68776b49caf3e12ac9d58d9402838cd3358e364b273b9ac05c5d40f14c`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 923.4 KB (923438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275b74970cb03c16331b016cd9939853b452f87372a86a4c40389b9c5be79036`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a25555d57ab3539ed771059c8521185b7ae6e80269f40f7c99f44b4d6951813`  
		Last Modified: Sat, 18 Oct 2025 00:29:20 GMT  
		Size: 11.7 MB (11657533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2362a39ea89169422cc185eb74c06b004d0dcedcb661947bf6b5fada1eec3b`  
		Last Modified: Sat, 18 Oct 2025 00:29:34 GMT  
		Size: 126.1 MB (126105923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba44311e3a69dfbf4bff73b14ec2e632021b964655cd313edb9dd67c3dbe287`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:02ae8eed66e146e5089f0b50e26900486150bed19c3b4ab916bfeeaeb02a9ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bffc43a9839864e7bbdf5a53b4fe85c6a51d22dd02630977801f7a9cfe94a40`

```dockerfile
```

-	Layers:
	-	`sha256:212e7e2ed7c9bf01d71763f91c84af92f9a7fdcc3be9cb21487e49dd147df03c`  
		Last Modified: Sat, 18 Oct 2025 03:45:51 GMT  
		Size: 3.3 MB (3340058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96566977bfe6f9660e00f242377960d0344565ccc624d780087c19d7aad1ea4e`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 32.6 KB (32554 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:e5d0f670d32e199f3716c2217f4cdd5d30ebbfb1fe878da07e36954a4ebd111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194740738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cce56a6f76c32dbcc85190738a1fbbe2f5e28f86d326208f5bde14dfa67ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bdd99e34712933a46f4c5e673752ba0902911086ef21b0fd05e75298983d0`  
		Last Modified: Wed, 08 Oct 2025 23:36:42 GMT  
		Size: 49.2 MB (49171450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413aa9ff83db8d823557459e1067061c28ec022d0903e0c8d585379b803368f2`  
		Last Modified: Wed, 08 Oct 2025 23:24:04 GMT  
		Size: 1.3 MB (1260561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515a3451535d72e062ce7b4ad2ec3061d8237bac9325d48cf6640b9b2bfb9c6`  
		Last Modified: Wed, 08 Oct 2025 23:24:08 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d54d0234216e5ee50b6c50ad8fdbbc79a766aac6dd54f0f0dbae8b27e780b`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427c8ab41e6da116a5d6ceff26ea4fcc2bc67ebb3be6cf183c07fe6f5649569`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 889.1 KB (889104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2418b617ace496bf08e707ea72732efe91fd4f5db7bc647949dd2f1464db9`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13ceff8223b9c0da58baef50e8fe3ebc34e37ec8ccac45bd4ea8b8bbaa543ef`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 11.7 MB (11658915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192ca5aa7254be1abd81c4c13041176c295a950f1a915028e0d6170f1a680ac`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 127.5 MB (127489346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000fb46604660c74fd92f91a092c0be218483d49e4bb3574e591d56c8974a5f`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:615ebdb6f060e1d0e03f301922e3ecdc9671af9eabeac9d02e3374cefc787a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3b9d966f1fe5d4b5ddc2548b81e296d80ce15f4b2445b41b99ad0c543a484e`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c7cddcb6aa27438ac5bb9936bc52be204811ed7084452e04aa8c4774ab210`  
		Last Modified: Sat, 18 Oct 2025 03:45:56 GMT  
		Size: 32.5 KB (32471 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a9b07a213a28dfd4578d6c9d8dd06bf6f24a421e1fee28be39bcfe4c1c5cfb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced87ecaae4b043bb4783679034696a04c2737a6e00755ccd1cb7b9f0bbea4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bea9d721b81739ae5afd1f43120131a937526df8a6915bcc5e45623c9dc3b67`  
		Last Modified: Wed, 08 Oct 2025 23:53:57 GMT  
		Size: 48.5 MB (48468220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984624dfaf62780b5725d1309a1eb1c8cb1d14439d384d9a088b6855536569ac`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a0c86a699a44ef49e0e96f977a6d6c34b4ffaf0584fc92e46c0c8a7503bab`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f9110eb5d505dad4577030c2949259fd2773e8baaf4ad9da1c4d84e19dcf8`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 701.5 KB (701483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d87d3255e074041ee5f0a12b3c1ac2431419e9aeb052f6bbfa5782a278b6e`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 889.1 KB (889098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3483e2b8d336d6454583116a36d40c25fb8f7a16c958e9ec723d600d054e72`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb77968a89a9be12fa3fa96505d6b6d281b3bea7e4412ffa8a46d2028c32797`  
		Last Modified: Sat, 18 Oct 2025 00:31:43 GMT  
		Size: 11.7 MB (11651330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05980c28f231f956a3ed45f51a9d0b1aef67bf6cceff1a4359755619d3df298`  
		Last Modified: Sat, 18 Oct 2025 00:31:51 GMT  
		Size: 127.2 MB (127174816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c33eae9d972262247fc5c605723aa1186b38782cdf1e9d45ab4a019c09c269`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:336f27e6ea1cab5985ecfe2f1344d4ac0d33684c0dbd3acb27869511e850ed64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3369769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce55101537eca36370070a09e8e607e497917f5417e62bfda9dc1cf426e5d51`

```dockerfile
```

-	Layers:
	-	`sha256:aa2c0cfc7990958bb3a493fc455e7efcc5574f01b555329760327dbd2242544f`  
		Last Modified: Sat, 18 Oct 2025 03:45:59 GMT  
		Size: 3.3 MB (3337083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce534b3719e8f4ef66e95ec1b0974cf5871c9812dea861636656bcf361b4141`  
		Last Modified: Sat, 18 Oct 2025 03:46:00 GMT  
		Size: 32.7 KB (32686 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.4.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:98912b55682059cceb54c93973a7f25bb0eec4547b79b26176da014337cfeab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206874888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36db5a036f2c1e2cb52ed89b18108b95198dc7b64e07b8dc599a2aa908b0b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d61e981703581f111feeaf3584550c7b2b22ac5c57a260d76386576bad8c438`  
		Last Modified: Wed, 08 Oct 2025 22:44:22 GMT  
		Size: 51.2 MB (51199404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6507169272064be83968b71a12bac1a223eb06cffa85615ce0ad229fc6bc54`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846561b46d4c3d9791e970078963c3be4ce306bc370156b98f8182e8079f5`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8b4df016b28cd75d4087813cbce98ed88e94e31dc2e4af61c30d20ef5d7f1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 838.6 KB (838570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b95a0c3e08205cf3722856e1453d43185c5cfb3e62a928492082022ef8f89`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 876.4 KB (876366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ca8465c4106c99cc321da47509d129f031cfe8f765255226b8ae829204d5d1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3374586f03c6371486b749afe721e3d6a0892430d5f48d1b252f0ae845c746b7`  
		Last Modified: Sat, 18 Oct 2025 00:32:17 GMT  
		Size: 11.7 MB (11656937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6013f3a38fdf8e386e7e7359dbafff49de28d66f59f85d20b1dcb0f60c3d0fdf`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 136.9 MB (136903774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa87ec0ea679e4fe3e6426e246dc107584dc7e8b1f88d6ce8a074952bc3b7d8`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.4.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e08016234ab4d76c3bd758ff8687267d7d9f4708ae9129820d11b283b5933c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4788db0a4b56b72acdf053a5cc892e885dfafb70b9917282d44794258abcf63e`

```dockerfile
```

-	Layers:
	-	`sha256:e68121590c2a2a419a67d03d337e6d76f45dd11c961c091ff97e6a4f64d4293a`  
		Last Modified: Sat, 18 Oct 2025 03:46:03 GMT  
		Size: 3.3 MB (3340166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13969f68868d68b0bd533141c2264f7fc02d01055749ad77fa8d87b60b92872`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 32.7 KB (32718 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:8a72ec9676734569570538838cbda1ab2389578f68870eede3a018da83b3e7c1
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
$ docker pull ghost@sha256:12fbffc2e0df73204d397cca5ae44797be54f9991adca2671e151c450f2d6dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196013578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8b24d4ecd61186acfbeb1f28494dde035ca25fe041a9ed80b30def9504ff49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f385331c129e26191cd1be348031f074d5cef6ae65f0b4c575f5470aeeb5290`  
		Last Modified: Wed, 08 Oct 2025 23:11:39 GMT  
		Size: 51.5 MB (51485406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd7e47c1da3b1d6d5752f0fe515ebf93bef68421b4748c48302b6b6dddc0dc`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 1.3 MB (1260591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a43d49c5117bb6048f44499d8980962eb8c429b52ea12441d635c0c1c9a56b`  
		Last Modified: Wed, 08 Oct 2025 23:11:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb69ac78192fce08b521a9df89e18a8f7dc3a9105c50d1cc1189db1ff27c1f5`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 777.0 KB (777040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724ae68776b49caf3e12ac9d58d9402838cd3358e364b273b9ac05c5d40f14c`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 923.4 KB (923438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275b74970cb03c16331b016cd9939853b452f87372a86a4c40389b9c5be79036`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a25555d57ab3539ed771059c8521185b7ae6e80269f40f7c99f44b4d6951813`  
		Last Modified: Sat, 18 Oct 2025 00:29:20 GMT  
		Size: 11.7 MB (11657533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2362a39ea89169422cc185eb74c06b004d0dcedcb661947bf6b5fada1eec3b`  
		Last Modified: Sat, 18 Oct 2025 00:29:34 GMT  
		Size: 126.1 MB (126105923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba44311e3a69dfbf4bff73b14ec2e632021b964655cd313edb9dd67c3dbe287`  
		Last Modified: Sat, 18 Oct 2025 00:29:19 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:02ae8eed66e146e5089f0b50e26900486150bed19c3b4ab916bfeeaeb02a9ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bffc43a9839864e7bbdf5a53b4fe85c6a51d22dd02630977801f7a9cfe94a40`

```dockerfile
```

-	Layers:
	-	`sha256:212e7e2ed7c9bf01d71763f91c84af92f9a7fdcc3be9cb21487e49dd147df03c`  
		Last Modified: Sat, 18 Oct 2025 03:45:51 GMT  
		Size: 3.3 MB (3340058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96566977bfe6f9660e00f242377960d0344565ccc624d780087c19d7aad1ea4e`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 32.6 KB (32554 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:e5d0f670d32e199f3716c2217f4cdd5d30ebbfb1fe878da07e36954a4ebd111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194740738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cce56a6f76c32dbcc85190738a1fbbe2f5e28f86d326208f5bde14dfa67ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bdd99e34712933a46f4c5e673752ba0902911086ef21b0fd05e75298983d0`  
		Last Modified: Wed, 08 Oct 2025 23:36:42 GMT  
		Size: 49.2 MB (49171450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413aa9ff83db8d823557459e1067061c28ec022d0903e0c8d585379b803368f2`  
		Last Modified: Wed, 08 Oct 2025 23:24:04 GMT  
		Size: 1.3 MB (1260561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515a3451535d72e062ce7b4ad2ec3061d8237bac9325d48cf6640b9b2bfb9c6`  
		Last Modified: Wed, 08 Oct 2025 23:24:08 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d54d0234216e5ee50b6c50ad8fdbbc79a766aac6dd54f0f0dbae8b27e780b`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427c8ab41e6da116a5d6ceff26ea4fcc2bc67ebb3be6cf183c07fe6f5649569`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 889.1 KB (889104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2418b617ace496bf08e707ea72732efe91fd4f5db7bc647949dd2f1464db9`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13ceff8223b9c0da58baef50e8fe3ebc34e37ec8ccac45bd4ea8b8bbaa543ef`  
		Last Modified: Sat, 18 Oct 2025 00:31:29 GMT  
		Size: 11.7 MB (11658915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192ca5aa7254be1abd81c4c13041176c295a950f1a915028e0d6170f1a680ac`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 127.5 MB (127489346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000fb46604660c74fd92f91a092c0be218483d49e4bb3574e591d56c8974a5f`  
		Last Modified: Sat, 18 Oct 2025 00:31:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:615ebdb6f060e1d0e03f301922e3ecdc9671af9eabeac9d02e3374cefc787a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3b9d966f1fe5d4b5ddc2548b81e296d80ce15f4b2445b41b99ad0c543a484e`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c7cddcb6aa27438ac5bb9936bc52be204811ed7084452e04aa8c4774ab210`  
		Last Modified: Sat, 18 Oct 2025 03:45:56 GMT  
		Size: 32.5 KB (32471 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a9b07a213a28dfd4578d6c9d8dd06bf6f24a421e1fee28be39bcfe4c1c5cfb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced87ecaae4b043bb4783679034696a04c2737a6e00755ccd1cb7b9f0bbea4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bea9d721b81739ae5afd1f43120131a937526df8a6915bcc5e45623c9dc3b67`  
		Last Modified: Wed, 08 Oct 2025 23:53:57 GMT  
		Size: 48.5 MB (48468220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984624dfaf62780b5725d1309a1eb1c8cb1d14439d384d9a088b6855536569ac`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a0c86a699a44ef49e0e96f977a6d6c34b4ffaf0584fc92e46c0c8a7503bab`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f9110eb5d505dad4577030c2949259fd2773e8baaf4ad9da1c4d84e19dcf8`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 701.5 KB (701483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d87d3255e074041ee5f0a12b3c1ac2431419e9aeb052f6bbfa5782a278b6e`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 889.1 KB (889098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3483e2b8d336d6454583116a36d40c25fb8f7a16c958e9ec723d600d054e72`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb77968a89a9be12fa3fa96505d6b6d281b3bea7e4412ffa8a46d2028c32797`  
		Last Modified: Sat, 18 Oct 2025 00:31:43 GMT  
		Size: 11.7 MB (11651330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05980c28f231f956a3ed45f51a9d0b1aef67bf6cceff1a4359755619d3df298`  
		Last Modified: Sat, 18 Oct 2025 00:31:51 GMT  
		Size: 127.2 MB (127174816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c33eae9d972262247fc5c605723aa1186b38782cdf1e9d45ab4a019c09c269`  
		Last Modified: Sat, 18 Oct 2025 00:31:42 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:336f27e6ea1cab5985ecfe2f1344d4ac0d33684c0dbd3acb27869511e850ed64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3369769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce55101537eca36370070a09e8e607e497917f5417e62bfda9dc1cf426e5d51`

```dockerfile
```

-	Layers:
	-	`sha256:aa2c0cfc7990958bb3a493fc455e7efcc5574f01b555329760327dbd2242544f`  
		Last Modified: Sat, 18 Oct 2025 03:45:59 GMT  
		Size: 3.3 MB (3337083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce534b3719e8f4ef66e95ec1b0974cf5871c9812dea861636656bcf361b4141`  
		Last Modified: Sat, 18 Oct 2025 03:46:00 GMT  
		Size: 32.7 KB (32686 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:98912b55682059cceb54c93973a7f25bb0eec4547b79b26176da014337cfeab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206874888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36db5a036f2c1e2cb52ed89b18108b95198dc7b64e07b8dc599a2aa908b0b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="119817f0a2cb86e9b8f058a9fc0a9fcb1b56a8a6da7c6ebef64398328ee52d82" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d61e981703581f111feeaf3584550c7b2b22ac5c57a260d76386576bad8c438`  
		Last Modified: Wed, 08 Oct 2025 22:44:22 GMT  
		Size: 51.2 MB (51199404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6507169272064be83968b71a12bac1a223eb06cffa85615ce0ad229fc6bc54`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846561b46d4c3d9791e970078963c3be4ce306bc370156b98f8182e8079f5`  
		Last Modified: Wed, 08 Oct 2025 22:44:18 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8b4df016b28cd75d4087813cbce98ed88e94e31dc2e4af61c30d20ef5d7f1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 838.6 KB (838570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b95a0c3e08205cf3722856e1453d43185c5cfb3e62a928492082022ef8f89`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 876.4 KB (876366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ca8465c4106c99cc321da47509d129f031cfe8f765255226b8ae829204d5d1`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3374586f03c6371486b749afe721e3d6a0892430d5f48d1b252f0ae845c746b7`  
		Last Modified: Sat, 18 Oct 2025 00:32:17 GMT  
		Size: 11.7 MB (11656937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6013f3a38fdf8e386e7e7359dbafff49de28d66f59f85d20b1dcb0f60c3d0fdf`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 136.9 MB (136903774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa87ec0ea679e4fe3e6426e246dc107584dc7e8b1f88d6ce8a074952bc3b7d8`  
		Last Modified: Sat, 18 Oct 2025 00:32:16 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:e08016234ab4d76c3bd758ff8687267d7d9f4708ae9129820d11b283b5933c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4788db0a4b56b72acdf053a5cc892e885dfafb70b9917282d44794258abcf63e`

```dockerfile
```

-	Layers:
	-	`sha256:e68121590c2a2a419a67d03d337e6d76f45dd11c961c091ff97e6a4f64d4293a`  
		Last Modified: Sat, 18 Oct 2025 03:46:03 GMT  
		Size: 3.3 MB (3340166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13969f68868d68b0bd533141c2264f7fc02d01055749ad77fa8d87b60b92872`  
		Last Modified: Sat, 18 Oct 2025 03:46:04 GMT  
		Size: 32.7 KB (32718 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:7686d30f30383bb08df0dcd5c89fd897c4e2112d3f6a50f8ecdb78cf021bad2e
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
$ docker pull ghost@sha256:e0d477eca26277b7868de615763a27a8d75724bebdc72f8e42ba716d7d5f133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218576394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c46db0139e218d0602cd5e87b8e96145de5fa8a722502670a1eac235387378f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98ba22ffba63e671e794151a8c72b2dd2e2394a99dfdadb48375658423035c`  
		Last Modified: Tue, 21 Oct 2025 01:49:16 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce3834b70636fccfd15681ae09efc245e61d942555ff1b60eff662498f71f8`  
		Last Modified: Tue, 21 Oct 2025 01:49:20 GMT  
		Size: 49.4 MB (49406240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4168ab2bca6183681fd3571770924ab57da32eadefdb46f2208e8d8e572011`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e85ddc713935ca5a0accf8aec281f24ed3e23d93f11df909657e9ee9a0403`  
		Last Modified: Tue, 21 Oct 2025 01:49:17 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184228eff12de998e31c119c22628a0214103d642cb2565a8f3e8f63f443bb1`  
		Last Modified: Tue, 21 Oct 2025 05:05:15 GMT  
		Size: 1.2 MB (1247341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3edd59bde935bd9eb92e8a1d7062f172dff05ee19bd9154471d701aa16affd9`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 11.7 MB (11661483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46bdfee218799cc3f27d6745d89a93a4047bf50be50e3e2ee83cd465d74fc52`  
		Last Modified: Tue, 21 Oct 2025 05:05:23 GMT  
		Size: 126.3 MB (126316069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63b4f25f0e618fed546bcd79af50eaa4e82811670015b2e7e0a784fddb26d21`  
		Last Modified: Tue, 21 Oct 2025 05:05:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:6f4e0d84f80c4c7af9ea51d490fb0a102070b88740f56050d19d6d6cd3b9927e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4ac880fa060e58864e38bfa6a08c0084a3f01ca86672c61cdba47104730bf`

```dockerfile
```

-	Layers:
	-	`sha256:e7d16010c082e36f6352e043cc8ad362b86ee7ce147b43037b74ebbdf9e48814`  
		Last Modified: Tue, 21 Oct 2025 09:45:47 GMT  
		Size: 5.6 MB (5553963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0aa203325540398a2d4bb16fb5c221dc12e68ee0752c49dec8160b877b0c09`  
		Last Modified: Tue, 21 Oct 2025 09:45:48 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a8d79fc46cfa3b2146fa9fdd21dfb3b7268ba7494cd810b3ffe794d580823271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210030395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26bf23785bc61c442262280e3ac6923f91b3c3a6d757abe11c45c98aa1dae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b71629629a04cc6e17d182034fdc2181577adfa385f1edbfc4dd8bc3d17a38a`  
		Last Modified: Tue, 21 Oct 2025 02:57:36 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b787ce0420c13b5936470725c1246c0a56bb1980f368545047829b37396961`  
		Last Modified: Tue, 21 Oct 2025 02:57:38 GMT  
		Size: 44.1 MB (44136924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ab4cac8e6724a34f622a34a9016e857f8280ad0ec6152728226d371344e12`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 1.7 MB (1712852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e3d58d86740d69693dd91be91201911df44b63d9904f076ebe3cb30c5e100`  
		Last Modified: Tue, 21 Oct 2025 02:57:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636d5fe8a91c198d3cec1a0f69391c7eddc5173ef352005fb1b98d5931561b7`  
		Last Modified: Tue, 21 Oct 2025 04:34:23 GMT  
		Size: 1.2 MB (1214242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12442508853d21a7948b51aeaac6c3c97b6bf7e29dbe173e84d3ff56380823`  
		Last Modified: Tue, 21 Oct 2025 04:34:25 GMT  
		Size: 11.7 MB (11659902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27929b078986502b92d9386cf999508c186d976502094d31f9422209b7a3f459`  
		Last Modified: Tue, 21 Oct 2025 04:34:32 GMT  
		Size: 127.4 MB (127368126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879dbe16d2cc622be175350d82500f51f0c4cc0229b9f053c06df5f9e14be9c`  
		Last Modified: Tue, 21 Oct 2025 04:34:24 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:b995f50fb036806a6c149022b0542072ca38052d26b9431b53b0ff8e4d8e5b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5586422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21b6af0016282deb192da392c34d6668bf33eb2ccd7608019742163ef55a4`

```dockerfile
```

-	Layers:
	-	`sha256:b744f421054207dcfbfc26d2fa8b433cc2cad21922b9aea6d35cc72bc7537d62`  
		Last Modified: Tue, 21 Oct 2025 09:45:54 GMT  
		Size: 5.6 MB (5556730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359ef7cf0f362e274b5fdfce92bc56999680b403e589829b86579be6ad1e01bc`  
		Last Modified: Tue, 21 Oct 2025 09:45:55 GMT  
		Size: 29.7 KB (29692 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c47af56f42eb7a653433e87b4fb222c45558abd3a40c99702ed9ad7c9ac9104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218617983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e21c6c89aaad2f667bf50f8b18d9edf7ed7037fc2c817a40fc057f7afc9386c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6efb3d89d6fbb561172dac0bac32b6471b483864b886fe2c368f1067cdababc`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85423f326066e5b8f27da57b383099ab376e8c4a5aef811c6c3585a6c5408c51`  
		Last Modified: Tue, 21 Oct 2025 01:53:29 GMT  
		Size: 49.5 MB (49527078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be39782492fdb1e331910941d37268b079b5c40902a14bf080c011304f93678`  
		Last Modified: Tue, 21 Oct 2025 01:53:26 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bbe160aa659a28e1734f2db7b579f339cfe1318b77d8224d726a60791087ef`  
		Last Modified: Tue, 21 Oct 2025 01:53:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4ed615b323eed16b6eababfc34f00f2bd476d3ecc22dbe6c75b83316652e5`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 1.2 MB (1201368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561bc5c5a5ab4d1e1cf0e6b9ba23ae99b562ced5698d734cc78e86b06a589c4d`  
		Last Modified: Tue, 21 Oct 2025 02:55:29 GMT  
		Size: 11.7 MB (11664635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed1a2ab1ec332f0e972d6a60f41970f9741b0118134a4e9260cd616e2afb25`  
		Last Modified: Tue, 21 Oct 2025 02:55:42 GMT  
		Size: 126.4 MB (126405759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ef1ca878c2a6c23796070519927497295064b3716fbb5c6a2f9818a01bd9e1`  
		Last Modified: Tue, 21 Oct 2025 02:55:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:0c93fac739fe60f4f72635709e82f3c45ad9a864286dcab9c93d0a4464b53bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dc578c7ea8fcef555fe487fddf696c722448d11b02cd58ea682a2a49f84a30`

```dockerfile
```

-	Layers:
	-	`sha256:312b73581d5cf7220f576a145f5e58ed1f134653d0a349fcc99f6702cd06ed42`  
		Last Modified: Tue, 21 Oct 2025 09:46:00 GMT  
		Size: 5.6 MB (5554266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cda9550065f120bf2273bb59be7890c430bc005bdf298e0271670e357e792f`  
		Last Modified: Tue, 21 Oct 2025 09:46:01 GMT  
		Size: 29.7 KB (29720 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:12c318536387a510d4778defab8940dbc4a0c3b4cafb2c9ad1c24566d0948085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229242707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2681de0a58f99ad4817eacfe98c0be6d2ebd096fa024f3c0985c5fae6f2139a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba7755b2a53d0c79e094ab3a53620f312430fd6488a999f0312ba7266fc090`  
		Last Modified: Tue, 30 Sep 2025 02:46:17 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9450cb0ad48e77b8c7761b8d7fa9475ff419eb4a608d4f32cd964f9a72670`  
		Last Modified: Tue, 30 Sep 2025 02:48:33 GMT  
		Size: 52.3 MB (52337574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6b4d67e724f98a40f227d607e8b19f8c022311f853dff99d21082838be5cc`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 1.7 MB (1712763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99f21b04f5204e1b4372936a87d3f5c9b6e17b55765bcba9cc5e26c8516a33e`  
		Last Modified: Tue, 30 Sep 2025 02:48:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e8ae3158969af71841027c5c4fb9383637b9a508b42c1ed4dfc98ac4e5d47`  
		Last Modified: Thu, 09 Oct 2025 18:34:34 GMT  
		Size: 1.2 MB (1206289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847f4b8f0e3e298ced64127f395fedfeaec0be21be8d9ddb828f1ad0bb0177`  
		Last Modified: Thu, 09 Oct 2025 18:34:36 GMT  
		Size: 11.7 MB (11656635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cce27bc0d5228a740cb51459bcdf46a0432a4edb389f7e28e452a0a47ea568`  
		Last Modified: Sat, 18 Oct 2025 12:01:37 GMT  
		Size: 130.3 MB (130256418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e27719d9e048ccb9e7d727c637b7da293c04d8fa10f43aec70311461877a671`  
		Last Modified: Sat, 18 Oct 2025 00:34:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:88ba8763237f9d0f1c30c4877c64c2d16731eddb12be1b20b07878e9b14e9b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5582663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726272f6f5390fa97e3283252b511318d9f20138a88ea678591f49293c2d2c8`

```dockerfile
```

-	Layers:
	-	`sha256:8b5e7e918af2e24e3268578ef18f68bf9454d19aa8d65bb79199a1209d48f26c`  
		Last Modified: Sat, 18 Oct 2025 03:45:52 GMT  
		Size: 5.6 MB (5553029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b58d9d49d4fe0d4fbb6e80a147e65e90d9ebecb4bb1c865116509751d258c4`  
		Last Modified: Sat, 18 Oct 2025 03:45:53 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:afd7a11b44a684e29f7e4a35f951b562bb2d2130a65b46d06bfc7dca267d9233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220526578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d0fdb3c1d0f3ac8a2089f6ec012b219cca0a5abb2c01f9b3df625b14784d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Sep 2025 14:35:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 24 Sep 2025 14:35:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV NODE_VERSION=22.20.0
# Wed, 24 Sep 2025 14:35:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENV YARN_VERSION=1.22.22
# Wed, 24 Sep 2025 14:35:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Sep 2025 14:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Sep 2025 14:35:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbcbdea5c0cfcece7050c4981d65bc0d3d44e48ed890be33bb9adb9cf005989`  
		Last Modified: Tue, 30 Sep 2025 03:30:13 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1ef775861addedb3c47f18021d9a8fbdf772f8cd1d622722de95d54eed3c8f`  
		Last Modified: Tue, 30 Sep 2025 03:31:27 GMT  
		Size: 49.6 MB (49590828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67806ce7ef92e8d06544d92ebc309872ff6c32287bff4cb5a9664962e95a359`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 1.7 MB (1712584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2bfded38c5ae1160660e490c3743aae01c21ea3b80049ceca9825514a964cf`  
		Last Modified: Tue, 30 Sep 2025 03:31:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f6c1312c799b5711fa348eb696800f3947f641f37d80109b438cc3fcf5835`  
		Last Modified: Thu, 09 Oct 2025 18:56:28 GMT  
		Size: 1.2 MB (1221134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fea8d7ebe3962eded038f9c7f2c02df3bffd9b603d05cc54f25e4a5e5c72585`  
		Last Modified: Thu, 09 Oct 2025 18:56:29 GMT  
		Size: 11.7 MB (11667690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f66e9132158eff2abb1b4642609b348ad0a4a0734dad97ae6c83ac2ca886b4`  
		Last Modified: Sat, 18 Oct 2025 18:42:04 GMT  
		Size: 129.4 MB (129445694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3502cf0d044992d10453795fc317fc6f47b69c6cef8875b704a1eaec767d5f88`  
		Last Modified: Sat, 18 Oct 2025 00:30:18 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:918cd556a5732d3b8ddcb2b8001a1f4590e944350b88c80efc50706a2580afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5576585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0a94915b1692e192f20275994e574c3c1c18964796d51cf1940f1101d2d054`

```dockerfile
```

-	Layers:
	-	`sha256:633bce997aedcc74f5037b7b76886fe32ce9beadd8c0eebe7cd0d34066c43963`  
		Last Modified: Sat, 18 Oct 2025 03:45:57 GMT  
		Size: 5.5 MB (5546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459a34e959e8ab2a3e782ba19bffb9b62bccc7f8e8273b14bdbd779fbdb271aa`  
		Last Modified: Sat, 18 Oct 2025 03:45:58 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

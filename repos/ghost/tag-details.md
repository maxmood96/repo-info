<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.110`](#ghost5110)
-	[`ghost:5.110-alpine`](#ghost5110-alpine)
-	[`ghost:5.110.1`](#ghost51101)
-	[`ghost:5.110.1-alpine`](#ghost51101-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:9de4b8fb21bffdf2bb17e590ca72c653e76e32f96dae258b851a052b2b4eb05f
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
$ docker pull ghost@sha256:1c3a13ab1bae977d91cb4a2151be0338c49e1650a1a7ade07969047d93cd3c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171711695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0774ff88e9dce936af4222b7e6dd58d7003a9a7ebddc7566cdd044ebeb216674`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb523f9949d5a7daf6db82dad36148d5db94842b019a5ff3b46a37e5ca8c477`  
		Last Modified: Thu, 20 Feb 2025 15:28:08 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7a7595b13a798b287fa6f5f7cdfb15fe827ae29d263faeee1f7c7c974596fc`  
		Last Modified: Thu, 20 Feb 2025 15:28:10 GMT  
		Size: 38.2 MB (38238343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5099d4dbd43f80c0fd6e8fa3dd431a8b1ef8bd51bd2cf7720efa00ba4c356d`  
		Last Modified: Thu, 20 Feb 2025 15:28:09 GMT  
		Size: 1.7 MB (1712407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa8e9fdbb06b52f6cfeffbae1b6d180d8a970a35d03bf977a36f44b9694276`  
		Last Modified: Thu, 20 Feb 2025 15:28:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df947333732ea9f5db6d0edf6da931ad356d2ec3abb76637c2e776d8f4c4b15`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 1.4 MB (1444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a5457173f702f12870484343795ea7be4f9b938ef1043b09a6b167bf917536`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 11.0 MB (10954592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b2bcb2d6bce7936f7386c472860588310148b0f081d59f868386ade38ab3f`  
		Last Modified: Sat, 22 Feb 2025 00:30:53 GMT  
		Size: 91.1 MB (91145011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07941442a5f72a95bf8a608e0eb412fd1bf04134f11121594819d0ca6f89b4eb`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:f45ae208569d1d859b35d7565025b46e6ac5484d04198aba7cc08441f759ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5463851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9ff9d87fb2a5280aaa81ace81b2c68a0ee28345ee7f14acf11441229d2b594`

```dockerfile
```

-	Layers:
	-	`sha256:a00e14a4e945d5923b411d7b29746d38c6dedde2b70fd2452137cc17a48fd747`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 5.4 MB (5434545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223c8a3e855c0ed8d1cb4242f4bf3b7495d0ad5c8f8c07ef19e8001177223dab`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 29.3 KB (29306 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:3de96e83a47826fcb9cc0dbb0c171321a068c994622fa18f5035be44450c58c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184342193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93592fa461fda3496980fd59a7c3e10820815a01245a87bcd063a9c7a1012e4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8cb48b701f961b8b69a2f21dd1b0935bedb5b4695b9870730f50debd90412`  
		Last Modified: Tue, 04 Feb 2025 11:20:21 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a549058fe92f0cefaea2a9b620d60cc3714d877af1d34ffbc865a0d57faedc`  
		Last Modified: Thu, 20 Feb 2025 16:58:03 GMT  
		Size: 34.9 MB (34909845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc61399b5ba57bf4f4130b0ac4c2482424b00ac22345d486cb527e973f63c6`  
		Last Modified: Thu, 20 Feb 2025 16:58:02 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c7b7f1b451b12431a3a6e0db1fffdee1643d99e51836f21bfdfa54e781b86`  
		Last Modified: Thu, 20 Feb 2025 16:58:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa17f9e53c2e2ba8dddc0e43aaf9e51b0d8cdf2a3e20411cbeb7ccec9dce13aa`  
		Last Modified: Thu, 20 Feb 2025 17:15:44 GMT  
		Size: 1.4 MB (1412413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0b984ff6c15d3579b16def2834f4586c1a6ca37064db324dd4af6bffe6a180`  
		Last Modified: Thu, 20 Feb 2025 17:15:44 GMT  
		Size: 11.0 MB (10955994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aaa507d1fa7534c2892e7a58a5e2aa20e9393c9cdafc726ef420272fb93ddb`  
		Last Modified: Sat, 22 Feb 2025 04:33:37 GMT  
		Size: 111.4 MB (111432417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c544b3e2149567939a4389fdb9d797bb306c5053d12610a0dac68676c3e156`  
		Last Modified: Sat, 22 Feb 2025 04:33:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:163feb02028d7e2507d2097ceafafd8434f2140731086706d371e8c07773f066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a75da7002fd766313d3a826c27f03dc916a5ba65dd7669bb1b79ce7125dfe2`

```dockerfile
```

-	Layers:
	-	`sha256:eee6b2bab05778d1201212e82a5d5331ac5821bf494fa1be6ca1d0d6958fe77e`  
		Last Modified: Sat, 22 Feb 2025 04:33:34 GMT  
		Size: 5.4 MB (5440015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026b1758cdacc2d4b52ab0f6f81d3425b25599d435f38d08c4e4da4716f2b50f`  
		Last Modified: Sat, 22 Feb 2025 04:33:33 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0ee0fb3f4c410cbb48d85edede0c927050cd170fec7bf96bf48de6a08f80f1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172500998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a6ef273a42ef819abea8460bbc7fe03914b7dd0eda97ab128dbf84d88d24b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2476b939e8425ff9be0988aab8c0840cd3dd98bd6d23be088bbc335515cb4b5d`  
		Last Modified: Tue, 11 Feb 2025 00:22:26 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50abc6dac927edde9b5ea8a01493c887a43d3f9a0ab00de3c5fbb0cfa469e950`  
		Last Modified: Thu, 20 Feb 2025 16:14:19 GMT  
		Size: 38.3 MB (38306704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbb78fbd3816726bca7d344edf9af76fe63371c181dda8ef4fcddab23d68015`  
		Last Modified: Thu, 20 Feb 2025 16:14:17 GMT  
		Size: 1.7 MB (1712486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdec2937da4533759fae07a4bcffb523fec4a70c840998978663740baaf88c0`  
		Last Modified: Thu, 20 Feb 2025 16:14:17 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4dfe91bd3b978108a88784c72c091b08cae59b382740d9a3f907baa3ea5926`  
		Last Modified: Thu, 20 Feb 2025 17:09:26 GMT  
		Size: 1.4 MB (1376565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383777d25a258f8d50b5fce6a715adb64b6f00605bdc008136f26fb7c1ba3e57`  
		Last Modified: Thu, 20 Feb 2025 17:09:27 GMT  
		Size: 11.0 MB (10955018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79aef35196c8db6e64b7e86319a9c8ed9db0790f78845552c76bb6595b56403`  
		Last Modified: Sat, 22 Feb 2025 02:41:18 GMT  
		Size: 92.1 MB (92105006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b56321ab6284d4d6fad74407fc50379ae031d18dd0936023c2c535f44bd187`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:4445ed8db9c0f290e1475538b50a98b842d5ab2edb7dd79db95c3d475406e8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38267325836ffc536b448fb2850f552fde4375ed65571a841e1e76c8cd5bbe9`

```dockerfile
```

-	Layers:
	-	`sha256:e068cdad362f3e04261668aa86d58dc4464edb4e0129483a83328e1f185f4922`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 5.4 MB (5434796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9032659d1a1a6c216ad0d7c1f27d075ea43e99c7d343b77d205b4f684cfd8f9`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 29.4 KB (29441 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:e8242a26b52ac4976e96a83ebf1fae2fd61246cd1d9abcc63c11f62e1cfedd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185057174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7991555c71906473143eb5986fd123b6d42add7651838eb5e7437d24c85dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda1249ee400c8e0988e06b8e4aec48065f28cc5755b11179df786b1885d0792`  
		Last Modified: Tue, 11 Feb 2025 00:05:44 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f8b288dbfcb75b6f320ecabf1f5a6ca7152d47a4061db83814ba1cdbdd6287`  
		Last Modified: Thu, 20 Feb 2025 16:02:34 GMT  
		Size: 40.4 MB (40353058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffb2a45920eeb055b4b3ab5fdd3e95638668d47b4d173e5403eb921f839d478`  
		Last Modified: Thu, 20 Feb 2025 16:02:32 GMT  
		Size: 1.7 MB (1712704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eb74921a58e92e1591d7c8bda09f18cca1ac49da9cc7395345132750b811f`  
		Last Modified: Thu, 20 Feb 2025 16:02:31 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53627b05265d055bb0dc42096ad25bfd76d22fbab1e42d893c5f2bd1d04702`  
		Last Modified: Thu, 20 Feb 2025 16:19:07 GMT  
		Size: 1.4 MB (1366704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f8d673c160129abbf5fcf91d776b56565ce8e7d6887104ac89dd3257e9ebf4`  
		Last Modified: Thu, 20 Feb 2025 16:19:07 GMT  
		Size: 11.0 MB (10958722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b0dd990a4f180cd122a5f6559fa9b2acea62488f3c357d65262e0a15a5f861`  
		Last Modified: Sat, 22 Feb 2025 01:28:36 GMT  
		Size: 98.6 MB (98616866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81537abadcbe909af7766c12dc609cf2ba038846b3615015cc1a8ca0fd1dcdd`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:ca32f3b80c3bd440d3d7d318a50379f5999b5e13eae7dcb14ac383ac61787c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f92b07c018d16a567dc5f72616130361e0b116f343b887bfa96d8559b05afa`

```dockerfile
```

-	Layers:
	-	`sha256:cc71c9c7ac30ea97b30c530f3cdb863dc8dd8ffc218a81ab0e3f8f9cb4c24e95`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 5.4 MB (5430810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f477cce1b2f39a4c31e6265e99dc6995bff027ea3ca5c8d4473c5a726b0946e6`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 29.4 KB (29355 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:6e1b3253e5248d11bd0e2832da7785ecaf0b9113a1b509b67c043bb35aba59d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178021558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ea27c81d12f1600379515be13495370a7d6429035cd5d1d179552ef50da23a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f19a5f2eb8575e7c974c55d860a11cc4da254a8432e07ab52eb1db69e0525`  
		Last Modified: Tue, 11 Feb 2025 00:46:15 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31feebf4830af4de50a3da52de1bd28d2bb066365a881c11b97433e47e117646`  
		Last Modified: Thu, 20 Feb 2025 16:54:44 GMT  
		Size: 38.5 MB (38488505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452242d6548c8df93f722ff4f32c41ebcc9d6849efa6addc8f7c6874ec08957`  
		Last Modified: Thu, 20 Feb 2025 16:54:42 GMT  
		Size: 1.7 MB (1712472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2420947dcdd3ac143354b72fc63d4f8afcd913b1643574f153d949be4f2c5`  
		Last Modified: Thu, 20 Feb 2025 16:54:42 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1183f0ad0de4fdb835799171514f5387237cba7cd20a68f5ea01c9b36e2f4f`  
		Last Modified: Thu, 20 Feb 2025 17:14:49 GMT  
		Size: 1.4 MB (1410104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f0b8d28c8d958ffe2119c6276ff40702bdbb10cdeeb74c706134f1ab1f64a`  
		Last Modified: Thu, 20 Feb 2025 17:14:50 GMT  
		Size: 11.0 MB (10953960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca830fb1ec975cbfef3ea540b13903382cbd48df1ff8eaf197cf5ddd2468e966`  
		Last Modified: Sat, 22 Feb 2025 01:27:55 GMT  
		Size: 98.6 MB (98593562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d6a6a696cdcd9353a9bcd8eb990c0dc0f1fd289d995a6bc4e6c035b8fe6db6`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:9aa5064da8c61e2e2515deac63304d628968934514e43492f1321d81b85e035a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b483223aa7202cd16e8b780d48ed74fa7d6f935e73a2be811ba7a7827a2ec4`

```dockerfile
```

-	Layers:
	-	`sha256:fe2a0c0c9146de7d5a678304ee469956b7bc68334c1fa7bb17d220fe6b37eee0`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 5.4 MB (5426282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed163b11a1161c49f9505fda12371d827cc998d7375271405e7881daf4bb5af8`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:b73c66490a4a66a9f2f6c1b1d05e724de55b117e4328b77834ef695512267ce5
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
$ docker pull ghost@sha256:d3edcf2980c5ef3710947b258d67d64c02f7bda7abcd46c1e1d3833946db6769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146100991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7978337fa64b4416a22a59e74c74f5b18fbfad7bf6c2140fe9abc1b1429aaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cf150cb3746a8af43a656f15a671bb84fa704ac2413cf1e57cc37d12afa838`  
		Last Modified: Thu, 20 Feb 2025 15:27:48 GMT  
		Size: 40.0 MB (40013170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46e519824fbb18a1df4becc0a40665f5c1cd193e527b3b0e26683d10f140916`  
		Last Modified: Thu, 20 Feb 2025 15:27:47 GMT  
		Size: 1.3 MB (1260569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8c59f7308dbad7c144c50d7f2b78bdbb5ee2f158009c4c17aa8bdf56d74db0`  
		Last Modified: Thu, 20 Feb 2025 15:27:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff34a42c588a8051982a7d0debde58739599ccd2d7b7e1f9d676901cd9f1330`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 776.0 KB (775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d900aa25d648f7df827560b2fa5bfc160778b551e327ca5d48968a971f1b26f1`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 1.1 MB (1122672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2bddf34d2e1afa73a0e39f1988a74e9345ca0a3f049bf5799d2684d029a5b3`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731c6316ffeaee37d2e513668aaf9076290fb0d9ff481b12684b5c18651b6f71`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 11.0 MB (10954601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cefc571547c4ca2eaa8da9f1627997a367fd50c72fd5172f1ebe02da787a035`  
		Last Modified: Sat, 22 Feb 2025 00:31:10 GMT  
		Size: 88.3 MB (88330540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9d89662ca7f6a12adf64d08ed6f20c20f0a97a10adcce4e70c573136010e29`  
		Last Modified: Sat, 22 Feb 2025 00:31:08 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4450f4ddea0302a3fb1274098279f98bbd42db7ab03b41b38db8a5aac35a7150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9555a159ac591809036ae888d263a6105c11698a49fb66b778aa4cfe8d41d6`

```dockerfile
```

-	Layers:
	-	`sha256:9610ef5b0e97c365c22e6b5022b5a52ab63fc13419aea7bf2b1f62cc12dee628`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 3.3 MB (3328926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb37bff16f13ed3db541dd4826caaf6142e6be720e3393bdece7937cc86c4060`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 32.3 KB (32281 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2f782475df849b3e25f965389485e3e471c41ace1d888227391df1839987f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152593219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7aad7cc4218b48a303907dacf2b1f639aab155e7fe7f7f5577cede96bfdffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea40d65d8b0fb24acd97d819aaa0bd4da35cf5ca08041fec46b9be523cd99f75`  
		Last Modified: Thu, 20 Feb 2025 16:55:59 GMT  
		Size: 38.4 MB (38387843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf47db1c1bf6fac636be30982a9d9724eb0980fde421c0a286424adc58b6472`  
		Last Modified: Thu, 20 Feb 2025 16:55:58 GMT  
		Size: 1.3 MB (1260557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b277c943f3cfa56c3325390a9aedd99251ed54f6811d2da9e8e0cb6c4173e32e`  
		Last Modified: Thu, 20 Feb 2025 16:55:58 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf940e66500f5675e3e1fc8d00c502f97f21559279a4018db839ace9757f4801`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 765.0 KB (765029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d5850d85d116ae478bf950f64e1c0623892c6958a5d1e814512c53ff4433d9`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 1.1 MB (1090090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bb85883846ffa72235d67824ecf88880104afe4ee2ba16dbd2551d09ea9d5d`  
		Last Modified: Thu, 20 Feb 2025 17:16:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf25b8667986864e984cc563d17e21eb0f24e02770122d477f618d0d999a483`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 11.0 MB (10956690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed49e3897c76aee27f6be17e6f086a5ec111f9e3c44747a5047b4e2e32820492`  
		Last Modified: Sat, 22 Feb 2025 01:28:47 GMT  
		Size: 96.8 MB (96767087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d777c94e2cbacf96e50db67b34013df507dc17e7eb515da2297e3db4b5f693`  
		Last Modified: Sat, 22 Feb 2025 01:28:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c63e49d0d2c775457e40e0458c2816e3be0fed9ff939ca3be419125819d7408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0adca5b8b9fddb397e120931d7cdffaca9845f829addbe8c3c5e60d902526a`

```dockerfile
```

-	Layers:
	-	`sha256:84aab79a60eb64069f106061e4a992a09c6e7901a7bad6e2792941093a62f158`  
		Last Modified: Sat, 22 Feb 2025 01:28:44 GMT  
		Size: 32.2 KB (32194 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e8827fcca62697449ea81a4f489f625ef25a79087df42c1afa6709cc8e82f6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3023fb7423787373fe9737fadab0323a307e6c0b62164a5b47dd82ad543093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e9250f8d37860295660cb6888cf2a9cd07e9f8273d358fbfcc5b91b186c71`  
		Last Modified: Thu, 20 Feb 2025 16:56:40 GMT  
		Size: 37.9 MB (37880526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd516c43a9c8c1a6071910d627c97baf0bbf576bab45dfe06fc2b531edc6f9a6`  
		Last Modified: Thu, 20 Feb 2025 16:56:39 GMT  
		Size: 1.3 MB (1260565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de14ae62ec98b67cf4ab306d8a13fd85c622ffc897bc15ee634c9cbd94cf2c86`  
		Last Modified: Thu, 20 Feb 2025 16:56:38 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c5d2ba3693594163a6148f1eeafe074a1264ee6f7b5f65261ce78f4b4590c5`  
		Last Modified: Thu, 20 Feb 2025 17:22:40 GMT  
		Size: 700.6 KB (700636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31409e3734099c67809926e314a24f3fa932880cdf7a4aca7b3d06c568bc92`  
		Last Modified: Thu, 20 Feb 2025 17:22:41 GMT  
		Size: 1.1 MB (1090089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df22e9073694e53d4185e4d75cf169830b59d8159e1c57660ce4a764c36d97c7`  
		Last Modified: Thu, 20 Feb 2025 17:22:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3f4ccc8ff2011a9602f4cab9fccb73fe82646419e65df6140ccd88992060d`  
		Last Modified: Thu, 20 Feb 2025 17:22:41 GMT  
		Size: 11.0 MB (10955451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0096a8c77a404c56e1d034fab51ae3732b3b08582d4fa12798753853722ddbc7`  
		Last Modified: Sat, 22 Feb 2025 04:40:02 GMT  
		Size: 96.5 MB (96459638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3a09aaadb034c276a3de57510ea9bf558081c32f2e8085c11f22717eda250`  
		Last Modified: Sat, 22 Feb 2025 04:39:58 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a38512116c9f39b7fd95c161f6666f04a042efccf7bf9c64c384610d82fa4045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfdf753eb024b7db57cdaf9a06a059df6efb2c1275eb245cdca552c300bdacb`

```dockerfile
```

-	Layers:
	-	`sha256:ad4723e22b815b62cd0c961d1b495a30750cce66f051f92c6283be04616a30d9`  
		Last Modified: Sat, 22 Feb 2025 04:39:59 GMT  
		Size: 3.3 MB (3320969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64012c0642ab5638cfff6db6dc8c87014f8eb83385a3b81a06af2a417cddd16b`  
		Last Modified: Sat, 22 Feb 2025 04:39:58 GMT  
		Size: 32.4 KB (32409 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:322744b7cf3472ee5310a20eaeeb9bf23215c4c791c098e80db9c9918d53a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166210359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c79c597cc7337964213bad117321d0695c7d7e7444c31578fa2145b047ce40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaa9ad1194b5237604a21f51136a10074db38fcce2ca5d0f8c1464ea7cd58b5`  
		Last Modified: Thu, 20 Feb 2025 16:12:06 GMT  
		Size: 39.7 MB (39659230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cf66406b72936b2387727c74e7d79df27ee69c2605a8d7a7c45a039dd39153`  
		Last Modified: Thu, 20 Feb 2025 16:12:05 GMT  
		Size: 1.3 MB (1260605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9177602ed83f293f4532017fee734d15bf15bfefb453208e73a1e14443e66f6`  
		Last Modified: Thu, 20 Feb 2025 16:12:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f703fa374824eb766eb49d45a9a1cd64930d26afc4bf3b532792e8352f75b99d`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 837.5 KB (837453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55017a35fc49c6577e551fce2ba7283862c8338a070f3659d67111e759e8a3c`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 1.1 MB (1054503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2aa3a04a3b7942b8e47e43c979b7d0bc7680547fe9da0f4f51bc57ea5046b0`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb42e54acc657cf1c931c832b1af5a3e1f9fcc1cf3958fb48c5de4dba27b263a`  
		Last Modified: Thu, 20 Feb 2025 17:13:42 GMT  
		Size: 11.0 MB (10954750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d274a5c02bbcef77d956ebc99f0b83b3dcc7fecf7f2302d9dc3fc86634b8f3a`  
		Last Modified: Sat, 22 Feb 2025 02:45:19 GMT  
		Size: 108.4 MB (108449601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacdd4eec38745f298bfd0cc71604f1b3609bf84106b6d5e378e58a585c142f1`  
		Last Modified: Sat, 22 Feb 2025 02:45:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:967defd8daabb9a622bbb82c889a5717f7ef67293670f2087422996d8dbe0ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438436e56810de1c45117182d6c0f5646f73a5d0c481cdbba7527bb60ecae6cc`

```dockerfile
```

-	Layers:
	-	`sha256:a217ef3f4b3e35cb9d684cebf028b758775710d60d9beff526ab474a18ea822d`  
		Last Modified: Sat, 22 Feb 2025 02:45:16 GMT  
		Size: 3.3 MB (3328982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c56947edfc75aca85dc515042ac085258ce61eba43695c077fef3ed5301eb0`  
		Last Modified: Sat, 22 Feb 2025 02:45:15 GMT  
		Size: 32.4 KB (32447 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.110`

```console
$ docker pull ghost@sha256:9de4b8fb21bffdf2bb17e590ca72c653e76e32f96dae258b851a052b2b4eb05f
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

### `ghost:5.110` - linux; amd64

```console
$ docker pull ghost@sha256:1c3a13ab1bae977d91cb4a2151be0338c49e1650a1a7ade07969047d93cd3c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171711695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0774ff88e9dce936af4222b7e6dd58d7003a9a7ebddc7566cdd044ebeb216674`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb523f9949d5a7daf6db82dad36148d5db94842b019a5ff3b46a37e5ca8c477`  
		Last Modified: Thu, 20 Feb 2025 15:28:08 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7a7595b13a798b287fa6f5f7cdfb15fe827ae29d263faeee1f7c7c974596fc`  
		Last Modified: Thu, 20 Feb 2025 15:28:10 GMT  
		Size: 38.2 MB (38238343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5099d4dbd43f80c0fd6e8fa3dd431a8b1ef8bd51bd2cf7720efa00ba4c356d`  
		Last Modified: Thu, 20 Feb 2025 15:28:09 GMT  
		Size: 1.7 MB (1712407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa8e9fdbb06b52f6cfeffbae1b6d180d8a970a35d03bf977a36f44b9694276`  
		Last Modified: Thu, 20 Feb 2025 15:28:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df947333732ea9f5db6d0edf6da931ad356d2ec3abb76637c2e776d8f4c4b15`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 1.4 MB (1444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a5457173f702f12870484343795ea7be4f9b938ef1043b09a6b167bf917536`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 11.0 MB (10954592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b2bcb2d6bce7936f7386c472860588310148b0f081d59f868386ade38ab3f`  
		Last Modified: Sat, 22 Feb 2025 00:30:53 GMT  
		Size: 91.1 MB (91145011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07941442a5f72a95bf8a608e0eb412fd1bf04134f11121594819d0ca6f89b4eb`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110` - unknown; unknown

```console
$ docker pull ghost@sha256:f45ae208569d1d859b35d7565025b46e6ac5484d04198aba7cc08441f759ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5463851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9ff9d87fb2a5280aaa81ace81b2c68a0ee28345ee7f14acf11441229d2b594`

```dockerfile
```

-	Layers:
	-	`sha256:a00e14a4e945d5923b411d7b29746d38c6dedde2b70fd2452137cc17a48fd747`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 5.4 MB (5434545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223c8a3e855c0ed8d1cb4242f4bf3b7495d0ad5c8f8c07ef19e8001177223dab`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 29.3 KB (29306 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110` - linux; arm variant v7

```console
$ docker pull ghost@sha256:3de96e83a47826fcb9cc0dbb0c171321a068c994622fa18f5035be44450c58c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184342193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93592fa461fda3496980fd59a7c3e10820815a01245a87bcd063a9c7a1012e4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8cb48b701f961b8b69a2f21dd1b0935bedb5b4695b9870730f50debd90412`  
		Last Modified: Tue, 04 Feb 2025 11:20:21 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a549058fe92f0cefaea2a9b620d60cc3714d877af1d34ffbc865a0d57faedc`  
		Last Modified: Thu, 20 Feb 2025 16:58:03 GMT  
		Size: 34.9 MB (34909845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc61399b5ba57bf4f4130b0ac4c2482424b00ac22345d486cb527e973f63c6`  
		Last Modified: Thu, 20 Feb 2025 16:58:02 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c7b7f1b451b12431a3a6e0db1fffdee1643d99e51836f21bfdfa54e781b86`  
		Last Modified: Thu, 20 Feb 2025 16:58:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa17f9e53c2e2ba8dddc0e43aaf9e51b0d8cdf2a3e20411cbeb7ccec9dce13aa`  
		Last Modified: Thu, 20 Feb 2025 17:15:44 GMT  
		Size: 1.4 MB (1412413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0b984ff6c15d3579b16def2834f4586c1a6ca37064db324dd4af6bffe6a180`  
		Last Modified: Thu, 20 Feb 2025 17:15:44 GMT  
		Size: 11.0 MB (10955994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aaa507d1fa7534c2892e7a58a5e2aa20e9393c9cdafc726ef420272fb93ddb`  
		Last Modified: Sat, 22 Feb 2025 04:33:37 GMT  
		Size: 111.4 MB (111432417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c544b3e2149567939a4389fdb9d797bb306c5053d12610a0dac68676c3e156`  
		Last Modified: Sat, 22 Feb 2025 04:33:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110` - unknown; unknown

```console
$ docker pull ghost@sha256:163feb02028d7e2507d2097ceafafd8434f2140731086706d371e8c07773f066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a75da7002fd766313d3a826c27f03dc916a5ba65dd7669bb1b79ce7125dfe2`

```dockerfile
```

-	Layers:
	-	`sha256:eee6b2bab05778d1201212e82a5d5331ac5821bf494fa1be6ca1d0d6958fe77e`  
		Last Modified: Sat, 22 Feb 2025 04:33:34 GMT  
		Size: 5.4 MB (5440015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026b1758cdacc2d4b52ab0f6f81d3425b25599d435f38d08c4e4da4716f2b50f`  
		Last Modified: Sat, 22 Feb 2025 04:33:33 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0ee0fb3f4c410cbb48d85edede0c927050cd170fec7bf96bf48de6a08f80f1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172500998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a6ef273a42ef819abea8460bbc7fe03914b7dd0eda97ab128dbf84d88d24b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2476b939e8425ff9be0988aab8c0840cd3dd98bd6d23be088bbc335515cb4b5d`  
		Last Modified: Tue, 11 Feb 2025 00:22:26 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50abc6dac927edde9b5ea8a01493c887a43d3f9a0ab00de3c5fbb0cfa469e950`  
		Last Modified: Thu, 20 Feb 2025 16:14:19 GMT  
		Size: 38.3 MB (38306704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbb78fbd3816726bca7d344edf9af76fe63371c181dda8ef4fcddab23d68015`  
		Last Modified: Thu, 20 Feb 2025 16:14:17 GMT  
		Size: 1.7 MB (1712486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdec2937da4533759fae07a4bcffb523fec4a70c840998978663740baaf88c0`  
		Last Modified: Thu, 20 Feb 2025 16:14:17 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4dfe91bd3b978108a88784c72c091b08cae59b382740d9a3f907baa3ea5926`  
		Last Modified: Thu, 20 Feb 2025 17:09:26 GMT  
		Size: 1.4 MB (1376565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383777d25a258f8d50b5fce6a715adb64b6f00605bdc008136f26fb7c1ba3e57`  
		Last Modified: Thu, 20 Feb 2025 17:09:27 GMT  
		Size: 11.0 MB (10955018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79aef35196c8db6e64b7e86319a9c8ed9db0790f78845552c76bb6595b56403`  
		Last Modified: Sat, 22 Feb 2025 02:41:18 GMT  
		Size: 92.1 MB (92105006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b56321ab6284d4d6fad74407fc50379ae031d18dd0936023c2c535f44bd187`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110` - unknown; unknown

```console
$ docker pull ghost@sha256:4445ed8db9c0f290e1475538b50a98b842d5ab2edb7dd79db95c3d475406e8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38267325836ffc536b448fb2850f552fde4375ed65571a841e1e76c8cd5bbe9`

```dockerfile
```

-	Layers:
	-	`sha256:e068cdad362f3e04261668aa86d58dc4464edb4e0129483a83328e1f185f4922`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 5.4 MB (5434796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9032659d1a1a6c216ad0d7c1f27d075ea43e99c7d343b77d205b4f684cfd8f9`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 29.4 KB (29441 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110` - linux; ppc64le

```console
$ docker pull ghost@sha256:e8242a26b52ac4976e96a83ebf1fae2fd61246cd1d9abcc63c11f62e1cfedd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185057174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7991555c71906473143eb5986fd123b6d42add7651838eb5e7437d24c85dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda1249ee400c8e0988e06b8e4aec48065f28cc5755b11179df786b1885d0792`  
		Last Modified: Tue, 11 Feb 2025 00:05:44 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f8b288dbfcb75b6f320ecabf1f5a6ca7152d47a4061db83814ba1cdbdd6287`  
		Last Modified: Thu, 20 Feb 2025 16:02:34 GMT  
		Size: 40.4 MB (40353058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffb2a45920eeb055b4b3ab5fdd3e95638668d47b4d173e5403eb921f839d478`  
		Last Modified: Thu, 20 Feb 2025 16:02:32 GMT  
		Size: 1.7 MB (1712704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eb74921a58e92e1591d7c8bda09f18cca1ac49da9cc7395345132750b811f`  
		Last Modified: Thu, 20 Feb 2025 16:02:31 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53627b05265d055bb0dc42096ad25bfd76d22fbab1e42d893c5f2bd1d04702`  
		Last Modified: Thu, 20 Feb 2025 16:19:07 GMT  
		Size: 1.4 MB (1366704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f8d673c160129abbf5fcf91d776b56565ce8e7d6887104ac89dd3257e9ebf4`  
		Last Modified: Thu, 20 Feb 2025 16:19:07 GMT  
		Size: 11.0 MB (10958722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b0dd990a4f180cd122a5f6559fa9b2acea62488f3c357d65262e0a15a5f861`  
		Last Modified: Sat, 22 Feb 2025 01:28:36 GMT  
		Size: 98.6 MB (98616866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81537abadcbe909af7766c12dc609cf2ba038846b3615015cc1a8ca0fd1dcdd`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110` - unknown; unknown

```console
$ docker pull ghost@sha256:ca32f3b80c3bd440d3d7d318a50379f5999b5e13eae7dcb14ac383ac61787c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f92b07c018d16a567dc5f72616130361e0b116f343b887bfa96d8559b05afa`

```dockerfile
```

-	Layers:
	-	`sha256:cc71c9c7ac30ea97b30c530f3cdb863dc8dd8ffc218a81ab0e3f8f9cb4c24e95`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 5.4 MB (5430810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f477cce1b2f39a4c31e6265e99dc6995bff027ea3ca5c8d4473c5a726b0946e6`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 29.4 KB (29355 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110` - linux; s390x

```console
$ docker pull ghost@sha256:6e1b3253e5248d11bd0e2832da7785ecaf0b9113a1b509b67c043bb35aba59d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178021558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ea27c81d12f1600379515be13495370a7d6429035cd5d1d179552ef50da23a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f19a5f2eb8575e7c974c55d860a11cc4da254a8432e07ab52eb1db69e0525`  
		Last Modified: Tue, 11 Feb 2025 00:46:15 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31feebf4830af4de50a3da52de1bd28d2bb066365a881c11b97433e47e117646`  
		Last Modified: Thu, 20 Feb 2025 16:54:44 GMT  
		Size: 38.5 MB (38488505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452242d6548c8df93f722ff4f32c41ebcc9d6849efa6addc8f7c6874ec08957`  
		Last Modified: Thu, 20 Feb 2025 16:54:42 GMT  
		Size: 1.7 MB (1712472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2420947dcdd3ac143354b72fc63d4f8afcd913b1643574f153d949be4f2c5`  
		Last Modified: Thu, 20 Feb 2025 16:54:42 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1183f0ad0de4fdb835799171514f5387237cba7cd20a68f5ea01c9b36e2f4f`  
		Last Modified: Thu, 20 Feb 2025 17:14:49 GMT  
		Size: 1.4 MB (1410104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f0b8d28c8d958ffe2119c6276ff40702bdbb10cdeeb74c706134f1ab1f64a`  
		Last Modified: Thu, 20 Feb 2025 17:14:50 GMT  
		Size: 11.0 MB (10953960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca830fb1ec975cbfef3ea540b13903382cbd48df1ff8eaf197cf5ddd2468e966`  
		Last Modified: Sat, 22 Feb 2025 01:27:55 GMT  
		Size: 98.6 MB (98593562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d6a6a696cdcd9353a9bcd8eb990c0dc0f1fd289d995a6bc4e6c035b8fe6db6`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110` - unknown; unknown

```console
$ docker pull ghost@sha256:9aa5064da8c61e2e2515deac63304d628968934514e43492f1321d81b85e035a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b483223aa7202cd16e8b780d48ed74fa7d6f935e73a2be811ba7a7827a2ec4`

```dockerfile
```

-	Layers:
	-	`sha256:fe2a0c0c9146de7d5a678304ee469956b7bc68334c1fa7bb17d220fe6b37eee0`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 5.4 MB (5426282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed163b11a1161c49f9505fda12371d827cc998d7375271405e7881daf4bb5af8`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.110-alpine`

```console
$ docker pull ghost@sha256:b73c66490a4a66a9f2f6c1b1d05e724de55b117e4328b77834ef695512267ce5
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

### `ghost:5.110-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:d3edcf2980c5ef3710947b258d67d64c02f7bda7abcd46c1e1d3833946db6769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146100991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7978337fa64b4416a22a59e74c74f5b18fbfad7bf6c2140fe9abc1b1429aaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cf150cb3746a8af43a656f15a671bb84fa704ac2413cf1e57cc37d12afa838`  
		Last Modified: Thu, 20 Feb 2025 15:27:48 GMT  
		Size: 40.0 MB (40013170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46e519824fbb18a1df4becc0a40665f5c1cd193e527b3b0e26683d10f140916`  
		Last Modified: Thu, 20 Feb 2025 15:27:47 GMT  
		Size: 1.3 MB (1260569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8c59f7308dbad7c144c50d7f2b78bdbb5ee2f158009c4c17aa8bdf56d74db0`  
		Last Modified: Thu, 20 Feb 2025 15:27:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff34a42c588a8051982a7d0debde58739599ccd2d7b7e1f9d676901cd9f1330`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 776.0 KB (775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d900aa25d648f7df827560b2fa5bfc160778b551e327ca5d48968a971f1b26f1`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 1.1 MB (1122672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2bddf34d2e1afa73a0e39f1988a74e9345ca0a3f049bf5799d2684d029a5b3`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731c6316ffeaee37d2e513668aaf9076290fb0d9ff481b12684b5c18651b6f71`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 11.0 MB (10954601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cefc571547c4ca2eaa8da9f1627997a367fd50c72fd5172f1ebe02da787a035`  
		Last Modified: Sat, 22 Feb 2025 00:31:10 GMT  
		Size: 88.3 MB (88330540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9d89662ca7f6a12adf64d08ed6f20c20f0a97a10adcce4e70c573136010e29`  
		Last Modified: Sat, 22 Feb 2025 00:31:08 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4450f4ddea0302a3fb1274098279f98bbd42db7ab03b41b38db8a5aac35a7150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9555a159ac591809036ae888d263a6105c11698a49fb66b778aa4cfe8d41d6`

```dockerfile
```

-	Layers:
	-	`sha256:9610ef5b0e97c365c22e6b5022b5a52ab63fc13419aea7bf2b1f62cc12dee628`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 3.3 MB (3328926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb37bff16f13ed3db541dd4826caaf6142e6be720e3393bdece7937cc86c4060`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 32.3 KB (32281 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2f782475df849b3e25f965389485e3e471c41ace1d888227391df1839987f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152593219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7aad7cc4218b48a303907dacf2b1f639aab155e7fe7f7f5577cede96bfdffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea40d65d8b0fb24acd97d819aaa0bd4da35cf5ca08041fec46b9be523cd99f75`  
		Last Modified: Thu, 20 Feb 2025 16:55:59 GMT  
		Size: 38.4 MB (38387843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf47db1c1bf6fac636be30982a9d9724eb0980fde421c0a286424adc58b6472`  
		Last Modified: Thu, 20 Feb 2025 16:55:58 GMT  
		Size: 1.3 MB (1260557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b277c943f3cfa56c3325390a9aedd99251ed54f6811d2da9e8e0cb6c4173e32e`  
		Last Modified: Thu, 20 Feb 2025 16:55:58 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf940e66500f5675e3e1fc8d00c502f97f21559279a4018db839ace9757f4801`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 765.0 KB (765029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d5850d85d116ae478bf950f64e1c0623892c6958a5d1e814512c53ff4433d9`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 1.1 MB (1090090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bb85883846ffa72235d67824ecf88880104afe4ee2ba16dbd2551d09ea9d5d`  
		Last Modified: Thu, 20 Feb 2025 17:16:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf25b8667986864e984cc563d17e21eb0f24e02770122d477f618d0d999a483`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 11.0 MB (10956690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed49e3897c76aee27f6be17e6f086a5ec111f9e3c44747a5047b4e2e32820492`  
		Last Modified: Sat, 22 Feb 2025 01:28:47 GMT  
		Size: 96.8 MB (96767087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d777c94e2cbacf96e50db67b34013df507dc17e7eb515da2297e3db4b5f693`  
		Last Modified: Sat, 22 Feb 2025 01:28:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c63e49d0d2c775457e40e0458c2816e3be0fed9ff939ca3be419125819d7408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0adca5b8b9fddb397e120931d7cdffaca9845f829addbe8c3c5e60d902526a`

```dockerfile
```

-	Layers:
	-	`sha256:84aab79a60eb64069f106061e4a992a09c6e7901a7bad6e2792941093a62f158`  
		Last Modified: Sat, 22 Feb 2025 01:28:44 GMT  
		Size: 32.2 KB (32194 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e8827fcca62697449ea81a4f489f625ef25a79087df42c1afa6709cc8e82f6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3023fb7423787373fe9737fadab0323a307e6c0b62164a5b47dd82ad543093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e9250f8d37860295660cb6888cf2a9cd07e9f8273d358fbfcc5b91b186c71`  
		Last Modified: Thu, 20 Feb 2025 16:56:40 GMT  
		Size: 37.9 MB (37880526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd516c43a9c8c1a6071910d627c97baf0bbf576bab45dfe06fc2b531edc6f9a6`  
		Last Modified: Thu, 20 Feb 2025 16:56:39 GMT  
		Size: 1.3 MB (1260565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de14ae62ec98b67cf4ab306d8a13fd85c622ffc897bc15ee634c9cbd94cf2c86`  
		Last Modified: Thu, 20 Feb 2025 16:56:38 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c5d2ba3693594163a6148f1eeafe074a1264ee6f7b5f65261ce78f4b4590c5`  
		Last Modified: Thu, 20 Feb 2025 17:22:40 GMT  
		Size: 700.6 KB (700636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31409e3734099c67809926e314a24f3fa932880cdf7a4aca7b3d06c568bc92`  
		Last Modified: Thu, 20 Feb 2025 17:22:41 GMT  
		Size: 1.1 MB (1090089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df22e9073694e53d4185e4d75cf169830b59d8159e1c57660ce4a764c36d97c7`  
		Last Modified: Thu, 20 Feb 2025 17:22:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3f4ccc8ff2011a9602f4cab9fccb73fe82646419e65df6140ccd88992060d`  
		Last Modified: Thu, 20 Feb 2025 17:22:41 GMT  
		Size: 11.0 MB (10955451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0096a8c77a404c56e1d034fab51ae3732b3b08582d4fa12798753853722ddbc7`  
		Last Modified: Sat, 22 Feb 2025 04:40:02 GMT  
		Size: 96.5 MB (96459638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3a09aaadb034c276a3de57510ea9bf558081c32f2e8085c11f22717eda250`  
		Last Modified: Sat, 22 Feb 2025 04:39:58 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a38512116c9f39b7fd95c161f6666f04a042efccf7bf9c64c384610d82fa4045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfdf753eb024b7db57cdaf9a06a059df6efb2c1275eb245cdca552c300bdacb`

```dockerfile
```

-	Layers:
	-	`sha256:ad4723e22b815b62cd0c961d1b495a30750cce66f051f92c6283be04616a30d9`  
		Last Modified: Sat, 22 Feb 2025 04:39:59 GMT  
		Size: 3.3 MB (3320969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64012c0642ab5638cfff6db6dc8c87014f8eb83385a3b81a06af2a417cddd16b`  
		Last Modified: Sat, 22 Feb 2025 04:39:58 GMT  
		Size: 32.4 KB (32409 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.110-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:322744b7cf3472ee5310a20eaeeb9bf23215c4c791c098e80db9c9918d53a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166210359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c79c597cc7337964213bad117321d0695c7d7e7444c31578fa2145b047ce40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaa9ad1194b5237604a21f51136a10074db38fcce2ca5d0f8c1464ea7cd58b5`  
		Last Modified: Thu, 20 Feb 2025 16:12:06 GMT  
		Size: 39.7 MB (39659230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cf66406b72936b2387727c74e7d79df27ee69c2605a8d7a7c45a039dd39153`  
		Last Modified: Thu, 20 Feb 2025 16:12:05 GMT  
		Size: 1.3 MB (1260605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9177602ed83f293f4532017fee734d15bf15bfefb453208e73a1e14443e66f6`  
		Last Modified: Thu, 20 Feb 2025 16:12:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f703fa374824eb766eb49d45a9a1cd64930d26afc4bf3b532792e8352f75b99d`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 837.5 KB (837453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55017a35fc49c6577e551fce2ba7283862c8338a070f3659d67111e759e8a3c`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 1.1 MB (1054503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2aa3a04a3b7942b8e47e43c979b7d0bc7680547fe9da0f4f51bc57ea5046b0`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb42e54acc657cf1c931c832b1af5a3e1f9fcc1cf3958fb48c5de4dba27b263a`  
		Last Modified: Thu, 20 Feb 2025 17:13:42 GMT  
		Size: 11.0 MB (10954750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d274a5c02bbcef77d956ebc99f0b83b3dcc7fecf7f2302d9dc3fc86634b8f3a`  
		Last Modified: Sat, 22 Feb 2025 02:45:19 GMT  
		Size: 108.4 MB (108449601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacdd4eec38745f298bfd0cc71604f1b3609bf84106b6d5e378e58a585c142f1`  
		Last Modified: Sat, 22 Feb 2025 02:45:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.110-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:967defd8daabb9a622bbb82c889a5717f7ef67293670f2087422996d8dbe0ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438436e56810de1c45117182d6c0f5646f73a5d0c481cdbba7527bb60ecae6cc`

```dockerfile
```

-	Layers:
	-	`sha256:a217ef3f4b3e35cb9d684cebf028b758775710d60d9beff526ab474a18ea822d`  
		Last Modified: Sat, 22 Feb 2025 02:45:16 GMT  
		Size: 3.3 MB (3328982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c56947edfc75aca85dc515042ac085258ce61eba43695c077fef3ed5301eb0`  
		Last Modified: Sat, 22 Feb 2025 02:45:15 GMT  
		Size: 32.4 KB (32447 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.110.1`

**does not exist** (yet?)

## `ghost:5.110.1-alpine`

**does not exist** (yet?)

## `ghost:alpine`

```console
$ docker pull ghost@sha256:b73c66490a4a66a9f2f6c1b1d05e724de55b117e4328b77834ef695512267ce5
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
$ docker pull ghost@sha256:d3edcf2980c5ef3710947b258d67d64c02f7bda7abcd46c1e1d3833946db6769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146100991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7978337fa64b4416a22a59e74c74f5b18fbfad7bf6c2140fe9abc1b1429aaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cf150cb3746a8af43a656f15a671bb84fa704ac2413cf1e57cc37d12afa838`  
		Last Modified: Thu, 20 Feb 2025 15:27:48 GMT  
		Size: 40.0 MB (40013170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46e519824fbb18a1df4becc0a40665f5c1cd193e527b3b0e26683d10f140916`  
		Last Modified: Thu, 20 Feb 2025 15:27:47 GMT  
		Size: 1.3 MB (1260569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8c59f7308dbad7c144c50d7f2b78bdbb5ee2f158009c4c17aa8bdf56d74db0`  
		Last Modified: Thu, 20 Feb 2025 15:27:46 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff34a42c588a8051982a7d0debde58739599ccd2d7b7e1f9d676901cd9f1330`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 776.0 KB (775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d900aa25d648f7df827560b2fa5bfc160778b551e327ca5d48968a971f1b26f1`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 1.1 MB (1122672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2bddf34d2e1afa73a0e39f1988a74e9345ca0a3f049bf5799d2684d029a5b3`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731c6316ffeaee37d2e513668aaf9076290fb0d9ff481b12684b5c18651b6f71`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 11.0 MB (10954601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cefc571547c4ca2eaa8da9f1627997a367fd50c72fd5172f1ebe02da787a035`  
		Last Modified: Sat, 22 Feb 2025 00:31:10 GMT  
		Size: 88.3 MB (88330540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9d89662ca7f6a12adf64d08ed6f20c20f0a97a10adcce4e70c573136010e29`  
		Last Modified: Sat, 22 Feb 2025 00:31:08 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4450f4ddea0302a3fb1274098279f98bbd42db7ab03b41b38db8a5aac35a7150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9555a159ac591809036ae888d263a6105c11698a49fb66b778aa4cfe8d41d6`

```dockerfile
```

-	Layers:
	-	`sha256:9610ef5b0e97c365c22e6b5022b5a52ab63fc13419aea7bf2b1f62cc12dee628`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 3.3 MB (3328926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb37bff16f13ed3db541dd4826caaf6142e6be720e3393bdece7937cc86c4060`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 32.3 KB (32281 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2f782475df849b3e25f965389485e3e471c41ace1d888227391df1839987f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152593219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7aad7cc4218b48a303907dacf2b1f639aab155e7fe7f7f5577cede96bfdffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea40d65d8b0fb24acd97d819aaa0bd4da35cf5ca08041fec46b9be523cd99f75`  
		Last Modified: Thu, 20 Feb 2025 16:55:59 GMT  
		Size: 38.4 MB (38387843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf47db1c1bf6fac636be30982a9d9724eb0980fde421c0a286424adc58b6472`  
		Last Modified: Thu, 20 Feb 2025 16:55:58 GMT  
		Size: 1.3 MB (1260557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b277c943f3cfa56c3325390a9aedd99251ed54f6811d2da9e8e0cb6c4173e32e`  
		Last Modified: Thu, 20 Feb 2025 16:55:58 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf940e66500f5675e3e1fc8d00c502f97f21559279a4018db839ace9757f4801`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 765.0 KB (765029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d5850d85d116ae478bf950f64e1c0623892c6958a5d1e814512c53ff4433d9`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 1.1 MB (1090090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bb85883846ffa72235d67824ecf88880104afe4ee2ba16dbd2551d09ea9d5d`  
		Last Modified: Thu, 20 Feb 2025 17:16:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf25b8667986864e984cc563d17e21eb0f24e02770122d477f618d0d999a483`  
		Last Modified: Thu, 20 Feb 2025 17:16:29 GMT  
		Size: 11.0 MB (10956690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed49e3897c76aee27f6be17e6f086a5ec111f9e3c44747a5047b4e2e32820492`  
		Last Modified: Sat, 22 Feb 2025 01:28:47 GMT  
		Size: 96.8 MB (96767087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d777c94e2cbacf96e50db67b34013df507dc17e7eb515da2297e3db4b5f693`  
		Last Modified: Sat, 22 Feb 2025 01:28:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c63e49d0d2c775457e40e0458c2816e3be0fed9ff939ca3be419125819d7408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0adca5b8b9fddb397e120931d7cdffaca9845f829addbe8c3c5e60d902526a`

```dockerfile
```

-	Layers:
	-	`sha256:84aab79a60eb64069f106061e4a992a09c6e7901a7bad6e2792941093a62f158`  
		Last Modified: Sat, 22 Feb 2025 01:28:44 GMT  
		Size: 32.2 KB (32194 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e8827fcca62697449ea81a4f489f625ef25a79087df42c1afa6709cc8e82f6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3023fb7423787373fe9737fadab0323a307e6c0b62164a5b47dd82ad543093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e9250f8d37860295660cb6888cf2a9cd07e9f8273d358fbfcc5b91b186c71`  
		Last Modified: Thu, 20 Feb 2025 16:56:40 GMT  
		Size: 37.9 MB (37880526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd516c43a9c8c1a6071910d627c97baf0bbf576bab45dfe06fc2b531edc6f9a6`  
		Last Modified: Thu, 20 Feb 2025 16:56:39 GMT  
		Size: 1.3 MB (1260565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de14ae62ec98b67cf4ab306d8a13fd85c622ffc897bc15ee634c9cbd94cf2c86`  
		Last Modified: Thu, 20 Feb 2025 16:56:38 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c5d2ba3693594163a6148f1eeafe074a1264ee6f7b5f65261ce78f4b4590c5`  
		Last Modified: Thu, 20 Feb 2025 17:22:40 GMT  
		Size: 700.6 KB (700636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31409e3734099c67809926e314a24f3fa932880cdf7a4aca7b3d06c568bc92`  
		Last Modified: Thu, 20 Feb 2025 17:22:41 GMT  
		Size: 1.1 MB (1090089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df22e9073694e53d4185e4d75cf169830b59d8159e1c57660ce4a764c36d97c7`  
		Last Modified: Thu, 20 Feb 2025 17:22:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3f4ccc8ff2011a9602f4cab9fccb73fe82646419e65df6140ccd88992060d`  
		Last Modified: Thu, 20 Feb 2025 17:22:41 GMT  
		Size: 11.0 MB (10955451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0096a8c77a404c56e1d034fab51ae3732b3b08582d4fa12798753853722ddbc7`  
		Last Modified: Sat, 22 Feb 2025 04:40:02 GMT  
		Size: 96.5 MB (96459638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3a09aaadb034c276a3de57510ea9bf558081c32f2e8085c11f22717eda250`  
		Last Modified: Sat, 22 Feb 2025 04:39:58 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a38512116c9f39b7fd95c161f6666f04a042efccf7bf9c64c384610d82fa4045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfdf753eb024b7db57cdaf9a06a059df6efb2c1275eb245cdca552c300bdacb`

```dockerfile
```

-	Layers:
	-	`sha256:ad4723e22b815b62cd0c961d1b495a30750cce66f051f92c6283be04616a30d9`  
		Last Modified: Sat, 22 Feb 2025 04:39:59 GMT  
		Size: 3.3 MB (3320969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64012c0642ab5638cfff6db6dc8c87014f8eb83385a3b81a06af2a417cddd16b`  
		Last Modified: Sat, 22 Feb 2025 04:39:58 GMT  
		Size: 32.4 KB (32409 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:322744b7cf3472ee5310a20eaeeb9bf23215c4c791c098e80db9c9918d53a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166210359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c79c597cc7337964213bad117321d0695c7d7e7444c31578fa2145b047ce40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f582108b1fdbceb4c428c34ddc9ad6d61e1b8d8d2c53843138b571aa35b88039" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaa9ad1194b5237604a21f51136a10074db38fcce2ca5d0f8c1464ea7cd58b5`  
		Last Modified: Thu, 20 Feb 2025 16:12:06 GMT  
		Size: 39.7 MB (39659230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cf66406b72936b2387727c74e7d79df27ee69c2605a8d7a7c45a039dd39153`  
		Last Modified: Thu, 20 Feb 2025 16:12:05 GMT  
		Size: 1.3 MB (1260605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9177602ed83f293f4532017fee734d15bf15bfefb453208e73a1e14443e66f6`  
		Last Modified: Thu, 20 Feb 2025 16:12:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f703fa374824eb766eb49d45a9a1cd64930d26afc4bf3b532792e8352f75b99d`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 837.5 KB (837453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55017a35fc49c6577e551fce2ba7283862c8338a070f3659d67111e759e8a3c`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 1.1 MB (1054503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2aa3a04a3b7942b8e47e43c979b7d0bc7680547fe9da0f4f51bc57ea5046b0`  
		Last Modified: Thu, 20 Feb 2025 17:13:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb42e54acc657cf1c931c832b1af5a3e1f9fcc1cf3958fb48c5de4dba27b263a`  
		Last Modified: Thu, 20 Feb 2025 17:13:42 GMT  
		Size: 11.0 MB (10954750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d274a5c02bbcef77d956ebc99f0b83b3dcc7fecf7f2302d9dc3fc86634b8f3a`  
		Last Modified: Sat, 22 Feb 2025 02:45:19 GMT  
		Size: 108.4 MB (108449601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacdd4eec38745f298bfd0cc71604f1b3609bf84106b6d5e378e58a585c142f1`  
		Last Modified: Sat, 22 Feb 2025 02:45:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:967defd8daabb9a622bbb82c889a5717f7ef67293670f2087422996d8dbe0ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438436e56810de1c45117182d6c0f5646f73a5d0c481cdbba7527bb60ecae6cc`

```dockerfile
```

-	Layers:
	-	`sha256:a217ef3f4b3e35cb9d684cebf028b758775710d60d9beff526ab474a18ea822d`  
		Last Modified: Sat, 22 Feb 2025 02:45:16 GMT  
		Size: 3.3 MB (3328982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c56947edfc75aca85dc515042ac085258ce61eba43695c077fef3ed5301eb0`  
		Last Modified: Sat, 22 Feb 2025 02:45:15 GMT  
		Size: 32.4 KB (32447 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:9de4b8fb21bffdf2bb17e590ca72c653e76e32f96dae258b851a052b2b4eb05f
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
$ docker pull ghost@sha256:1c3a13ab1bae977d91cb4a2151be0338c49e1650a1a7ade07969047d93cd3c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171711695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0774ff88e9dce936af4222b7e6dd58d7003a9a7ebddc7566cdd044ebeb216674`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb523f9949d5a7daf6db82dad36148d5db94842b019a5ff3b46a37e5ca8c477`  
		Last Modified: Thu, 20 Feb 2025 15:28:08 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7a7595b13a798b287fa6f5f7cdfb15fe827ae29d263faeee1f7c7c974596fc`  
		Last Modified: Thu, 20 Feb 2025 15:28:10 GMT  
		Size: 38.2 MB (38238343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5099d4dbd43f80c0fd6e8fa3dd431a8b1ef8bd51bd2cf7720efa00ba4c356d`  
		Last Modified: Thu, 20 Feb 2025 15:28:09 GMT  
		Size: 1.7 MB (1712407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa8e9fdbb06b52f6cfeffbae1b6d180d8a970a35d03bf977a36f44b9694276`  
		Last Modified: Thu, 20 Feb 2025 15:28:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df947333732ea9f5db6d0edf6da931ad356d2ec3abb76637c2e776d8f4c4b15`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 1.4 MB (1444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a5457173f702f12870484343795ea7be4f9b938ef1043b09a6b167bf917536`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 11.0 MB (10954592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b2bcb2d6bce7936f7386c472860588310148b0f081d59f868386ade38ab3f`  
		Last Modified: Sat, 22 Feb 2025 00:30:53 GMT  
		Size: 91.1 MB (91145011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07941442a5f72a95bf8a608e0eb412fd1bf04134f11121594819d0ca6f89b4eb`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:f45ae208569d1d859b35d7565025b46e6ac5484d04198aba7cc08441f759ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5463851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9ff9d87fb2a5280aaa81ace81b2c68a0ee28345ee7f14acf11441229d2b594`

```dockerfile
```

-	Layers:
	-	`sha256:a00e14a4e945d5923b411d7b29746d38c6dedde2b70fd2452137cc17a48fd747`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 5.4 MB (5434545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223c8a3e855c0ed8d1cb4242f4bf3b7495d0ad5c8f8c07ef19e8001177223dab`  
		Last Modified: Sat, 22 Feb 2025 00:30:52 GMT  
		Size: 29.3 KB (29306 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:3de96e83a47826fcb9cc0dbb0c171321a068c994622fa18f5035be44450c58c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184342193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93592fa461fda3496980fd59a7c3e10820815a01245a87bcd063a9c7a1012e4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8cb48b701f961b8b69a2f21dd1b0935bedb5b4695b9870730f50debd90412`  
		Last Modified: Tue, 04 Feb 2025 11:20:21 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a549058fe92f0cefaea2a9b620d60cc3714d877af1d34ffbc865a0d57faedc`  
		Last Modified: Thu, 20 Feb 2025 16:58:03 GMT  
		Size: 34.9 MB (34909845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc61399b5ba57bf4f4130b0ac4c2482424b00ac22345d486cb527e973f63c6`  
		Last Modified: Thu, 20 Feb 2025 16:58:02 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c7b7f1b451b12431a3a6e0db1fffdee1643d99e51836f21bfdfa54e781b86`  
		Last Modified: Thu, 20 Feb 2025 16:58:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa17f9e53c2e2ba8dddc0e43aaf9e51b0d8cdf2a3e20411cbeb7ccec9dce13aa`  
		Last Modified: Thu, 20 Feb 2025 17:15:44 GMT  
		Size: 1.4 MB (1412413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0b984ff6c15d3579b16def2834f4586c1a6ca37064db324dd4af6bffe6a180`  
		Last Modified: Thu, 20 Feb 2025 17:15:44 GMT  
		Size: 11.0 MB (10955994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aaa507d1fa7534c2892e7a58a5e2aa20e9393c9cdafc726ef420272fb93ddb`  
		Last Modified: Sat, 22 Feb 2025 04:33:37 GMT  
		Size: 111.4 MB (111432417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c544b3e2149567939a4389fdb9d797bb306c5053d12610a0dac68676c3e156`  
		Last Modified: Sat, 22 Feb 2025 04:33:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:163feb02028d7e2507d2097ceafafd8434f2140731086706d371e8c07773f066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a75da7002fd766313d3a826c27f03dc916a5ba65dd7669bb1b79ce7125dfe2`

```dockerfile
```

-	Layers:
	-	`sha256:eee6b2bab05778d1201212e82a5d5331ac5821bf494fa1be6ca1d0d6958fe77e`  
		Last Modified: Sat, 22 Feb 2025 04:33:34 GMT  
		Size: 5.4 MB (5440015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026b1758cdacc2d4b52ab0f6f81d3425b25599d435f38d08c4e4da4716f2b50f`  
		Last Modified: Sat, 22 Feb 2025 04:33:33 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0ee0fb3f4c410cbb48d85edede0c927050cd170fec7bf96bf48de6a08f80f1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172500998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a6ef273a42ef819abea8460bbc7fe03914b7dd0eda97ab128dbf84d88d24b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2476b939e8425ff9be0988aab8c0840cd3dd98bd6d23be088bbc335515cb4b5d`  
		Last Modified: Tue, 11 Feb 2025 00:22:26 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50abc6dac927edde9b5ea8a01493c887a43d3f9a0ab00de3c5fbb0cfa469e950`  
		Last Modified: Thu, 20 Feb 2025 16:14:19 GMT  
		Size: 38.3 MB (38306704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbb78fbd3816726bca7d344edf9af76fe63371c181dda8ef4fcddab23d68015`  
		Last Modified: Thu, 20 Feb 2025 16:14:17 GMT  
		Size: 1.7 MB (1712486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdec2937da4533759fae07a4bcffb523fec4a70c840998978663740baaf88c0`  
		Last Modified: Thu, 20 Feb 2025 16:14:17 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4dfe91bd3b978108a88784c72c091b08cae59b382740d9a3f907baa3ea5926`  
		Last Modified: Thu, 20 Feb 2025 17:09:26 GMT  
		Size: 1.4 MB (1376565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383777d25a258f8d50b5fce6a715adb64b6f00605bdc008136f26fb7c1ba3e57`  
		Last Modified: Thu, 20 Feb 2025 17:09:27 GMT  
		Size: 11.0 MB (10955018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79aef35196c8db6e64b7e86319a9c8ed9db0790f78845552c76bb6595b56403`  
		Last Modified: Sat, 22 Feb 2025 02:41:18 GMT  
		Size: 92.1 MB (92105006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b56321ab6284d4d6fad74407fc50379ae031d18dd0936023c2c535f44bd187`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:4445ed8db9c0f290e1475538b50a98b842d5ab2edb7dd79db95c3d475406e8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38267325836ffc536b448fb2850f552fde4375ed65571a841e1e76c8cd5bbe9`

```dockerfile
```

-	Layers:
	-	`sha256:e068cdad362f3e04261668aa86d58dc4464edb4e0129483a83328e1f185f4922`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 5.4 MB (5434796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9032659d1a1a6c216ad0d7c1f27d075ea43e99c7d343b77d205b4f684cfd8f9`  
		Last Modified: Sat, 22 Feb 2025 02:41:16 GMT  
		Size: 29.4 KB (29441 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:e8242a26b52ac4976e96a83ebf1fae2fd61246cd1d9abcc63c11f62e1cfedd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185057174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7991555c71906473143eb5986fd123b6d42add7651838eb5e7437d24c85dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda1249ee400c8e0988e06b8e4aec48065f28cc5755b11179df786b1885d0792`  
		Last Modified: Tue, 11 Feb 2025 00:05:44 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f8b288dbfcb75b6f320ecabf1f5a6ca7152d47a4061db83814ba1cdbdd6287`  
		Last Modified: Thu, 20 Feb 2025 16:02:34 GMT  
		Size: 40.4 MB (40353058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffb2a45920eeb055b4b3ab5fdd3e95638668d47b4d173e5403eb921f839d478`  
		Last Modified: Thu, 20 Feb 2025 16:02:32 GMT  
		Size: 1.7 MB (1712704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eb74921a58e92e1591d7c8bda09f18cca1ac49da9cc7395345132750b811f`  
		Last Modified: Thu, 20 Feb 2025 16:02:31 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53627b05265d055bb0dc42096ad25bfd76d22fbab1e42d893c5f2bd1d04702`  
		Last Modified: Thu, 20 Feb 2025 16:19:07 GMT  
		Size: 1.4 MB (1366704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f8d673c160129abbf5fcf91d776b56565ce8e7d6887104ac89dd3257e9ebf4`  
		Last Modified: Thu, 20 Feb 2025 16:19:07 GMT  
		Size: 11.0 MB (10958722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b0dd990a4f180cd122a5f6559fa9b2acea62488f3c357d65262e0a15a5f861`  
		Last Modified: Sat, 22 Feb 2025 01:28:36 GMT  
		Size: 98.6 MB (98616866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81537abadcbe909af7766c12dc609cf2ba038846b3615015cc1a8ca0fd1dcdd`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:ca32f3b80c3bd440d3d7d318a50379f5999b5e13eae7dcb14ac383ac61787c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f92b07c018d16a567dc5f72616130361e0b116f343b887bfa96d8559b05afa`

```dockerfile
```

-	Layers:
	-	`sha256:cc71c9c7ac30ea97b30c530f3cdb863dc8dd8ffc218a81ab0e3f8f9cb4c24e95`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 5.4 MB (5430810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f477cce1b2f39a4c31e6265e99dc6995bff027ea3ca5c8d4473c5a726b0946e6`  
		Last Modified: Sat, 22 Feb 2025 01:28:33 GMT  
		Size: 29.4 KB (29355 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:6e1b3253e5248d11bd0e2832da7785ecaf0b9113a1b509b67c043bb35aba59d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178021558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ea27c81d12f1600379515be13495370a7d6429035cd5d1d179552ef50da23a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV NODE_ENV=production
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 21 Feb 2025 15:19:13 GMT
ENV GHOST_VERSION=5.110.0
# Fri, 21 Feb 2025 15:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
WORKDIR /var/lib/ghost
# Fri, 21 Feb 2025 15:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 21 Feb 2025 15:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 21 Feb 2025 15:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 15:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 21 Feb 2025 15:19:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f19a5f2eb8575e7c974c55d860a11cc4da254a8432e07ab52eb1db69e0525`  
		Last Modified: Tue, 11 Feb 2025 00:46:15 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31feebf4830af4de50a3da52de1bd28d2bb066365a881c11b97433e47e117646`  
		Last Modified: Thu, 20 Feb 2025 16:54:44 GMT  
		Size: 38.5 MB (38488505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452242d6548c8df93f722ff4f32c41ebcc9d6849efa6addc8f7c6874ec08957`  
		Last Modified: Thu, 20 Feb 2025 16:54:42 GMT  
		Size: 1.7 MB (1712472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2420947dcdd3ac143354b72fc63d4f8afcd913b1643574f153d949be4f2c5`  
		Last Modified: Thu, 20 Feb 2025 16:54:42 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1183f0ad0de4fdb835799171514f5387237cba7cd20a68f5ea01c9b36e2f4f`  
		Last Modified: Thu, 20 Feb 2025 17:14:49 GMT  
		Size: 1.4 MB (1410104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f0b8d28c8d958ffe2119c6276ff40702bdbb10cdeeb74c706134f1ab1f64a`  
		Last Modified: Thu, 20 Feb 2025 17:14:50 GMT  
		Size: 11.0 MB (10953960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca830fb1ec975cbfef3ea540b13903382cbd48df1ff8eaf197cf5ddd2468e966`  
		Last Modified: Sat, 22 Feb 2025 01:27:55 GMT  
		Size: 98.6 MB (98593562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d6a6a696cdcd9353a9bcd8eb990c0dc0f1fd289d995a6bc4e6c035b8fe6db6`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:9aa5064da8c61e2e2515deac63304d628968934514e43492f1321d81b85e035a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b483223aa7202cd16e8b780d48ed74fa7d6f935e73a2be811ba7a7827a2ec4`

```dockerfile
```

-	Layers:
	-	`sha256:fe2a0c0c9146de7d5a678304ee469956b7bc68334c1fa7bb17d220fe6b37eee0`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 5.4 MB (5426282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed163b11a1161c49f9505fda12371d827cc998d7375271405e7881daf4bb5af8`  
		Last Modified: Sat, 22 Feb 2025 01:27:53 GMT  
		Size: 29.3 KB (29307 bytes)  
		MIME: application/vnd.in-toto+json

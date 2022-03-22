<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:4`](#ghost4)
-	[`ghost:4-alpine`](#ghost4-alpine)
-	[`ghost:4.40`](#ghost440)
-	[`ghost:4.40-alpine`](#ghost440-alpine)
-	[`ghost:4.40.0`](#ghost4400)
-	[`ghost:4.40.0-alpine`](#ghost4400-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:4`

```console
$ docker pull ghost@sha256:8f5f8956bf0507cc4e1d1fd97bd0a40dcdad36e27330055cb3355a683e74692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4` - linux; amd64

```console
$ docker pull ghost@sha256:40009e56de3db4de60243e1e62c8f16fb49b00b3d5a7a0770b857dcf7b8aab45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148139873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce6a785b302d09270261554593de0515b71ecb032d9845d74c0fc5fd7ca2fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 13:00:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 21:50:00 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:50:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 21:50:35 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:50:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 21:50:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:50:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:50:47 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:04:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 00:04:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 00:04:43 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:04:44 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:05:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:32 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:20:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:20:37 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:20:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:20:37 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:20:37 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:20:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bc29d3bc64ca0852101d86667b4a0d1908f05fe0bfead140cf838c0be01bc3`  
		Last Modified: Thu, 17 Mar 2022 13:19:15 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a71a1d6cc6986624592a148f866355b9b90ddcd4a1f24be36b0f849d8c1044`  
		Last Modified: Fri, 18 Mar 2022 22:14:33 GMT  
		Size: 36.0 MB (36048047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5afd073302f60aad2c5067b89a976a5572fa262d0b60478970f307f8f94b97`  
		Last Modified: Fri, 18 Mar 2022 22:14:27 GMT  
		Size: 2.8 MB (2781848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5878f59eaa39846dd1173083e2e77dc140082be0efc61f7838c3403c6254b113`  
		Last Modified: Fri, 18 Mar 2022 22:14:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753aec878444f5bbf5b9e13544f6a3caf78aae1d01d506806f4b342c32623f2a`  
		Last Modified: Sat, 19 Mar 2022 00:09:27 GMT  
		Size: 1.4 MB (1448123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e282a0a274714713330c2ae37bb9aa1be203226d7ffd7de6eec07f2e35270c8`  
		Last Modified: Sat, 19 Mar 2022 00:09:31 GMT  
		Size: 9.6 MB (9567975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba50ac34f7d063eb291142ba6663fa92b6fa22f83af83d6ac81c45a985edf82`  
		Last Modified: Tue, 22 Mar 2022 01:22:28 GMT  
		Size: 66.9 MB (66912128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca556e8b36141f67594a9dc845b46b3d4f7f97af03cce35b90ab4bb48617284`  
		Last Modified: Tue, 22 Mar 2022 01:22:16 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm variant v7

```console
$ docker pull ghost@sha256:496e4906ab53cce4e3b11a603a6c690e04041a35f041feef37984a85905c0f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146919839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51074a20029823e0c80fbcdf0fba912ccb81421e46b76785c731b7eb26e987e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:47:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:50:57 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:51:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:51:48 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:52:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:52:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:52:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:52:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:22:42 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:23:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:23:10 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:23:10 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:23:59 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:57:33 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:05:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:05:28 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:05:29 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:05:29 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:05:30 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:05:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c69f71c16ec3df2b7d124845d1b3b6e6495150f4ea3398c32a390afffbf142`  
		Last Modified: Fri, 18 Mar 2022 17:06:49 GMT  
		Size: 4.2 KB (4166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b32ca858e17b62400e3e3939b76745bd091c2302dcb5a659f98f4036c58ad`  
		Last Modified: Sat, 19 Mar 2022 00:07:18 GMT  
		Size: 34.2 MB (34206692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2605fefc93565569e993984be795855508fc11258205a2f0ab736807a40c2c`  
		Last Modified: Sat, 19 Mar 2022 00:06:56 GMT  
		Size: 2.8 MB (2772408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649abf5b9f938b138570d940f0d8c3af7d265d4e26a25cf69fbd121df9381c`  
		Last Modified: Sat, 19 Mar 2022 00:06:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4041d8d2d15b52a58284107ec1fbc633900cce1fc07418607ed52ea1564428aa`  
		Last Modified: Sat, 19 Mar 2022 23:41:13 GMT  
		Size: 1.4 MB (1400322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04c308287b4673d9ba168fbb3d4cec8b9c7e8a9fe4ce8e8bab11f7a83658e18`  
		Last Modified: Sat, 19 Mar 2022 23:41:27 GMT  
		Size: 9.6 MB (9569190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af17b4d49e748753d815dd39cf5821fd799c9661f0abaf3b1647d224609fe020`  
		Last Modified: Tue, 22 Mar 2022 01:15:00 GMT  
		Size: 72.4 MB (72390962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092670288c46febff531959fa7f27513c2ca9c780ae8bbcfd90945b263032b6`  
		Last Modified: Tue, 22 Mar 2022 01:13:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ff551f487def98ff5a1f560a93046cc5ac2c95df28cc70f7cd6d88f631cc266
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154218519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c0be74ec3768fb3421c9b9c6a2b4d1d12d2a3e7e0002cd920f5d572ac544f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:20:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:50:24 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:50:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:50:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:51:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:51:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:51:04 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:41:23 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 17:41:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:41:34 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:41:35 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:42:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:42:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:41:06 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:44:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:44:18 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:44:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:44:23 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 09:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:44:28 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:44:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e302ce9f0603b4af265c90ba2a4807900c24096808fb68bf44300bd440542`  
		Last Modified: Thu, 17 Mar 2022 13:54:35 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98badb25d325c02976fab44804955d995b60a19fc609da8e3f1e642c52d898f9`  
		Last Modified: Sat, 19 Mar 2022 00:54:11 GMT  
		Size: 36.2 MB (36154505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5d43df9c11963e4b0e365e779e63981833ea41bdcc5d4db11c675fcc84fab3`  
		Last Modified: Sat, 19 Mar 2022 00:54:06 GMT  
		Size: 2.8 MB (2781278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad002987a7bae850089e45777bc9a362a9f8e3c656bdbbb26980ec4776d4704b`  
		Last Modified: Sat, 19 Mar 2022 00:54:05 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f6d4797a5cc96449c367b48271ff6c2fdb6908b35b0b9c4c548113d8535a9`  
		Last Modified: Sat, 19 Mar 2022 17:50:44 GMT  
		Size: 1.4 MB (1383662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cde83364d3aeeba3311efa235a8b37ae7bbe49fd46d82e326c8c363b094c82`  
		Last Modified: Sat, 19 Mar 2022 17:50:46 GMT  
		Size: 9.6 MB (9568502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be81ef1a0fd0acf9499a994c1da09ef250cbadcbc2faaeccd4bf84af6fda4956`  
		Last Modified: Tue, 22 Mar 2022 09:49:17 GMT  
		Size: 74.3 MB (74262518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c707d1882e7a22e27458c5bc3dab90eded7fce83699e2ba619cfaa97617bb07`  
		Last Modified: Tue, 22 Mar 2022 09:49:02 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; ppc64le

```console
$ docker pull ghost@sha256:e01cb2e12a3c0c6642d370fb6a62d94ef478d4d1984db86324228cc57edbd4ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155582038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8168e6014a1fff905f12c4432217b0ce1b9397f135365a5fcd4691868f7ae152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:54:03 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:06:48 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:11:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:11:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:14:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:14:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:14:53 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:46:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:47:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:47:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:47:55 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:49:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:49:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:49:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:42 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:54:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:55:01 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:55:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:55:04 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:55:09 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:55:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca53b81b04fce4349fb7d53e6c96231409ea54bc6d07808c393a268d8fcd78c3`  
		Last Modified: Fri, 18 Mar 2022 08:33:21 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307e188a803758441743ab6c2c16c58d32cd25920f05e601d9fa75c13f8ec1f4`  
		Last Modified: Sat, 19 Mar 2022 02:15:29 GMT  
		Size: 38.0 MB (37978420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a74008e734f41eb1091af470bca5677108b1eb61729b017bd6e96944fc1c1`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 2.8 MB (2782569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c9e81db75711e347d46105e0daee9e64692433ad3141a1cf1a52bca316993e`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d14ae585ca54d978c72b25f6580d1c2986a60f049aefed6a7146e58b8eb07da`  
		Last Modified: Sun, 20 Mar 2022 00:12:26 GMT  
		Size: 1.4 MB (1367834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4904132a0f018373255a9418743ef13604d402190eaf4737c0de15b28964951`  
		Last Modified: Sun, 20 Mar 2022 00:12:31 GMT  
		Size: 9.6 MB (9568608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f2ab968cb74f11279d0c7784eac2069dae1dd4e24e911ca465976b7508ea9e`  
		Last Modified: Tue, 22 Mar 2022 01:56:01 GMT  
		Size: 68.6 MB (68599661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231cbb386dec32edcb41b2680932b86df8d092267a1cc20cd8460d53e2de5fa1`  
		Last Modified: Tue, 22 Mar 2022 01:55:43 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; s390x

```console
$ docker pull ghost@sha256:fe87a6607cc14c1e6d541b390418e86d94ef0e6a2f1a5824ce2a34be28dd42fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147374040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7785b0540fceae7764559a39b1b6c6d004271adb765c9c7d1bf0a450eec91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:50:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:14:52 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:15:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:15:12 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:15:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:15:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:15:22 GMT
CMD ["node"]
# Sat, 19 Mar 2022 04:38:44 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 04:38:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 04:38:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 04:38:53 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 04:39:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 04:41:25 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 04:44:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 04:44:34 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 04:44:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 04:44:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 04:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 04:44:35 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 04:44:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722821cfaf9b99e01207f42d38caa8d0eea9818925d58a5d590057ff6271525d`  
		Last Modified: Thu, 17 Mar 2022 14:21:32 GMT  
		Size: 4.2 KB (4189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8924acd2003e404035ae30769a9ed0531c116ccfe4965f354999da4c593b38dc`  
		Last Modified: Fri, 18 Mar 2022 23:10:07 GMT  
		Size: 35.9 MB (35913738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c92724e1dbac9baa9b4949197499bd94e7abda3f1392dd48cc6f78fb23589`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 2.8 MB (2782997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f42e3d4bc22c450816fb2255b83b884ec091394d12aff4a84c65c1193e935a`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a61fd10dbc4124b4be87498e57bca3e89cab9d50ed7acf9934d6103e2b32eb`  
		Last Modified: Sat, 19 Mar 2022 04:42:48 GMT  
		Size: 1.4 MB (1434956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d6f9332f2c9557e6d14acdf3a51fb916f10fa41d64027309df97ce26b51dbc`  
		Last Modified: Sat, 19 Mar 2022 04:42:49 GMT  
		Size: 9.6 MB (9567431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb15d072ea322a0984e1bc07bc2080dbb63a6377aacd148ea5a7e6bb2ef70ab3`  
		Last Modified: Tue, 22 Mar 2022 04:45:09 GMT  
		Size: 68.0 MB (68013938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74647066b08d262304545c5cd408b3e338c2ba369d364130b19402b25f9787c`  
		Last Modified: Tue, 22 Mar 2022 04:44:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4-alpine`

```console
$ docker pull ghost@sha256:6fbb449ae5780a8b11233638f905ae05de86aa353e6873d1b314bedf24d323ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:a77e68ccf7dda2ee3792ddbe7410b135017da73587a3b92f2551a2151d3f9a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120273400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae8c19cb15f05412656942201f77c420d714951fc8fdb4e26842fdc91da84e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 21:48:35 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:48:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 21:48:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:48:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 21:48:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:48:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:48:56 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:07:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 00:07:07 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 00:07:07 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:07:07 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:07:34 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:20:40 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:21:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:21:49 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:21:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:21:49 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:21:49 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:21:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580248b309d4fecaf2f75f42a36796a166140238395d38d36e0d47b20dded70`  
		Last Modified: Fri, 18 Mar 2022 22:13:15 GMT  
		Size: 37.1 MB (37132855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539902d50a314143ea1ff8b98bee2aae6a9e66b7f102cd5b0ba0b3b21650132e`  
		Last Modified: Fri, 18 Mar 2022 22:13:07 GMT  
		Size: 2.4 MB (2358489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d60032af439ffa29833ceee54906865bfc7e32949f8a0643d3e1f7307d6e`  
		Last Modified: Fri, 18 Mar 2022 22:13:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d799310e8353a5bf7d35c0a576c8cc8a22f423a2268da6c937e55e512240daf`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87a58ecffcb615b1c9af4968b84fdfb44fd7f432d7d7c6087a14f7ba7f201e`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 816.9 KB (816859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf689cb927dd935805d71b57cb514cc956df63b009fc1453a79c668d2dad985d`  
		Last Modified: Sat, 19 Mar 2022 00:10:04 GMT  
		Size: 9.6 MB (9567883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ba8f128db30b568c1afb77c95580ad9ea781beedbf02c8e710cf6f5cef54`  
		Last Modified: Tue, 22 Mar 2022 01:22:57 GMT  
		Size: 67.6 MB (67568935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ccf55d8c338f0b82f1e2891980a21d7c3c6bd2459b3c5bb230c58d7c3abfa`  
		Last Modified: Tue, 22 Mar 2022 01:22:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:6eb1dcf99ed6f26af1b845ee6be822a8792ef60012e9f4c6e1b4d66048067c09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121481209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04611e77a27d6228f5b1763798b34668030f2fd913d3c6fd909a9b20bab8415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 19:31:23 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 19:47:55 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 19:47:56 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 19:48:04 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 19:48:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 19:48:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 19:48:06 GMT
CMD ["node"]
# Fri, 18 Mar 2022 21:05:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 18 Mar 2022 21:05:06 GMT
RUN apk add --no-cache 		bash
# Fri, 18 Mar 2022 21:05:06 GMT
ENV NODE_ENV=production
# Fri, 18 Mar 2022 21:05:06 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Fri, 18 Mar 2022 21:06:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 18 Mar 2022 21:06:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 18 Mar 2022 21:06:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:49:29 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 00:58:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 00:58:30 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 00:58:30 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 00:58:31 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 00:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 00:58:32 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 00:58:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd48496521270c1ba2c1d855bd715f617b59d6498e2e407b804b566b7678087`  
		Last Modified: Fri, 18 Mar 2022 20:47:14 GMT  
		Size: 36.2 MB (36198526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5599fde36163c1ebda1ad804a5b327cc1609b46263a91060b9fc3a835d328be9`  
		Last Modified: Fri, 18 Mar 2022 20:47:01 GMT  
		Size: 2.4 MB (2418192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18709050207fe0cf4803ac4f14090c67a8729cd62b866e31ae708d3b6e7b9166`  
		Last Modified: Fri, 18 Mar 2022 20:46:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af606d946314fedea65ebbae67cbd1cecf6a786558facb4b88f3f5739e15c45b`  
		Last Modified: Fri, 18 Mar 2022 21:17:09 GMT  
		Size: 11.0 KB (10977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0954b81f1ae01a7d7b8339d694eef033a3a078ca6a23c44e8934eb1c6229c0`  
		Last Modified: Fri, 18 Mar 2022 21:17:10 GMT  
		Size: 771.0 KB (770953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455c516cdd5fda37a751a4a4b7ef0e58ecb18b7c3fb786fb1f485daa97406bee`  
		Last Modified: Fri, 18 Mar 2022 21:17:19 GMT  
		Size: 9.6 MB (9569616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c7fbc400c37ccd72196b5ce76baac59ecf3caac1ffed927371e017585928ab`  
		Last Modified: Tue, 22 Mar 2022 01:00:33 GMT  
		Size: 69.9 MB (69882585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee202258538a801abcb089b73edb50aedd95524c1ea3bb6e48507e0e12cff5`  
		Last Modified: Tue, 22 Mar 2022 00:59:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:0644cf2d840856b3b3b40294c669e01ddcc682aea78116a58f4411bd42e64a74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a949fc5edc87eb366eafe3542807d0cce220766ee5d07bde46387085a173034`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 22:22:50 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:36:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 22:36:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:36:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 22:36:17 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:36:18 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:32:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 23:32:12 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 23:32:13 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:32:13 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:33:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:33:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:33:07 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:05:44 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:12:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:12:57 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:12:58 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:12:58 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:12:59 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:12:59 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7fb7593e1ec2c0060c773dbbf85fcbe77df0a45cbc891cd7f775442f959ce6`  
		Last Modified: Sat, 19 Mar 2022 00:04:50 GMT  
		Size: 35.8 MB (35750941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b531d0f3fa4a8c1e5c8c32c0c6a9de8cda1e078ed43db62853858f7ef792044b`  
		Last Modified: Sat, 19 Mar 2022 00:04:27 GMT  
		Size: 2.4 MB (2418360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ead18221dfbeb2afd1c7044892b00c01b6b056d5feb01c74684dff97d67e8eb`  
		Last Modified: Sat, 19 Mar 2022 00:04:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1faeeef23a40a6e07406285a95e3f94a86314cef806a54bbf3e2672288624dc`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 10.8 KB (10772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41729cace1ddd94023eba72c5c881b17ee1ab0e939be1d113c4f144fdae876c1`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 703.9 KB (703890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca1f8edf6ec39144c3fa34019e53bf9892978c935ab4b45e035f61c9cd7e32b`  
		Last Modified: Sat, 19 Mar 2022 23:42:57 GMT  
		Size: 9.6 MB (9569052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da276e29c5e8450fa177e6d44587e3deaf6cfd77e57b31dc25d000b5f5ccfd`  
		Last Modified: Tue, 22 Mar 2022 01:16:33 GMT  
		Size: 69.4 MB (69352758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee60ff28d8cf519c5f76cf745628e7c194ebe3f1ba8c04ad29aa550de0d86f`  
		Last Modified: Tue, 22 Mar 2022 01:15:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c3acf9a8c79217eac40fc9d89cec24c52d29d2831b2d2e8face8145b35bdff92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139988964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56691249b0321d0f36da40f17d7967c308221441d74557bf9032398ab19dbb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 23:07:29 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:28:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 23:28:15 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:28:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 23:28:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:28:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:28:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:45:45 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 17:45:47 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 17:45:47 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:45:48 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:46:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:46:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:46:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:44:48 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:48:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:48:24 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:48:27 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:48:29 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 09:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:48:34 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:48:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c992e90d8c9f9d1552190d2c0c3fa8fb5e94e39970cd9453e2819dc8b40ec1`  
		Last Modified: Sat, 19 Mar 2022 00:52:52 GMT  
		Size: 37.0 MB (37013909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc77e26b629b7d5ec72075b9db80763d03618483ac484e3129801b1b8131c6fe`  
		Last Modified: Sat, 19 Mar 2022 00:52:45 GMT  
		Size: 2.4 MB (2425472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36be0e7c4d5b1efb3a4be2317e16421a2d536fefec860c776192b0e5447a112`  
		Last Modified: Sat, 19 Mar 2022 00:52:44 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f881f7c1a27e3be051f3f7a6dc8e2234929511ade4258d41308f3b54ac77285`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ed0c2707cfd63880efce177bce0dc0dcb620859f33f8eb2c8661ad10a49e5`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 826.0 KB (826035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b3448e3e9cafa84aaabc148a2d7dff4a9270250a65345e20bf35c1c76c37`  
		Last Modified: Sat, 19 Mar 2022 17:51:19 GMT  
		Size: 9.6 MB (9567877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58636e87905f213f67950f1595df76af6261b3839115ec785486bdc81be9aed`  
		Last Modified: Tue, 22 Mar 2022 09:49:51 GMT  
		Size: 87.4 MB (87427790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be17ef9ec12b78c3e972aca3d3acfd1718fa34340d87ebadf1cb2a111bee70`  
		Last Modified: Tue, 22 Mar 2022 09:49:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.40`

```console
$ docker pull ghost@sha256:8f5f8956bf0507cc4e1d1fd97bd0a40dcdad36e27330055cb3355a683e74692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.40` - linux; amd64

```console
$ docker pull ghost@sha256:40009e56de3db4de60243e1e62c8f16fb49b00b3d5a7a0770b857dcf7b8aab45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148139873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce6a785b302d09270261554593de0515b71ecb032d9845d74c0fc5fd7ca2fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 13:00:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 21:50:00 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:50:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 21:50:35 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:50:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 21:50:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:50:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:50:47 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:04:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 00:04:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 00:04:43 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:04:44 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:05:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:32 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:20:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:20:37 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:20:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:20:37 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:20:37 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:20:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bc29d3bc64ca0852101d86667b4a0d1908f05fe0bfead140cf838c0be01bc3`  
		Last Modified: Thu, 17 Mar 2022 13:19:15 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a71a1d6cc6986624592a148f866355b9b90ddcd4a1f24be36b0f849d8c1044`  
		Last Modified: Fri, 18 Mar 2022 22:14:33 GMT  
		Size: 36.0 MB (36048047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5afd073302f60aad2c5067b89a976a5572fa262d0b60478970f307f8f94b97`  
		Last Modified: Fri, 18 Mar 2022 22:14:27 GMT  
		Size: 2.8 MB (2781848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5878f59eaa39846dd1173083e2e77dc140082be0efc61f7838c3403c6254b113`  
		Last Modified: Fri, 18 Mar 2022 22:14:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753aec878444f5bbf5b9e13544f6a3caf78aae1d01d506806f4b342c32623f2a`  
		Last Modified: Sat, 19 Mar 2022 00:09:27 GMT  
		Size: 1.4 MB (1448123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e282a0a274714713330c2ae37bb9aa1be203226d7ffd7de6eec07f2e35270c8`  
		Last Modified: Sat, 19 Mar 2022 00:09:31 GMT  
		Size: 9.6 MB (9567975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba50ac34f7d063eb291142ba6663fa92b6fa22f83af83d6ac81c45a985edf82`  
		Last Modified: Tue, 22 Mar 2022 01:22:28 GMT  
		Size: 66.9 MB (66912128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca556e8b36141f67594a9dc845b46b3d4f7f97af03cce35b90ab4bb48617284`  
		Last Modified: Tue, 22 Mar 2022 01:22:16 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40` - linux; arm variant v7

```console
$ docker pull ghost@sha256:496e4906ab53cce4e3b11a603a6c690e04041a35f041feef37984a85905c0f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146919839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51074a20029823e0c80fbcdf0fba912ccb81421e46b76785c731b7eb26e987e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:47:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:50:57 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:51:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:51:48 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:52:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:52:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:52:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:52:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:22:42 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:23:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:23:10 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:23:10 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:23:59 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:57:33 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:05:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:05:28 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:05:29 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:05:29 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:05:30 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:05:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c69f71c16ec3df2b7d124845d1b3b6e6495150f4ea3398c32a390afffbf142`  
		Last Modified: Fri, 18 Mar 2022 17:06:49 GMT  
		Size: 4.2 KB (4166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b32ca858e17b62400e3e3939b76745bd091c2302dcb5a659f98f4036c58ad`  
		Last Modified: Sat, 19 Mar 2022 00:07:18 GMT  
		Size: 34.2 MB (34206692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2605fefc93565569e993984be795855508fc11258205a2f0ab736807a40c2c`  
		Last Modified: Sat, 19 Mar 2022 00:06:56 GMT  
		Size: 2.8 MB (2772408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649abf5b9f938b138570d940f0d8c3af7d265d4e26a25cf69fbd121df9381c`  
		Last Modified: Sat, 19 Mar 2022 00:06:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4041d8d2d15b52a58284107ec1fbc633900cce1fc07418607ed52ea1564428aa`  
		Last Modified: Sat, 19 Mar 2022 23:41:13 GMT  
		Size: 1.4 MB (1400322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04c308287b4673d9ba168fbb3d4cec8b9c7e8a9fe4ce8e8bab11f7a83658e18`  
		Last Modified: Sat, 19 Mar 2022 23:41:27 GMT  
		Size: 9.6 MB (9569190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af17b4d49e748753d815dd39cf5821fd799c9661f0abaf3b1647d224609fe020`  
		Last Modified: Tue, 22 Mar 2022 01:15:00 GMT  
		Size: 72.4 MB (72390962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092670288c46febff531959fa7f27513c2ca9c780ae8bbcfd90945b263032b6`  
		Last Modified: Tue, 22 Mar 2022 01:13:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ff551f487def98ff5a1f560a93046cc5ac2c95df28cc70f7cd6d88f631cc266
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154218519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c0be74ec3768fb3421c9b9c6a2b4d1d12d2a3e7e0002cd920f5d572ac544f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:20:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:50:24 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:50:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:50:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:51:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:51:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:51:04 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:41:23 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 17:41:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:41:34 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:41:35 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:42:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:42:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:41:06 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:44:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:44:18 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:44:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:44:23 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 09:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:44:28 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:44:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e302ce9f0603b4af265c90ba2a4807900c24096808fb68bf44300bd440542`  
		Last Modified: Thu, 17 Mar 2022 13:54:35 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98badb25d325c02976fab44804955d995b60a19fc609da8e3f1e642c52d898f9`  
		Last Modified: Sat, 19 Mar 2022 00:54:11 GMT  
		Size: 36.2 MB (36154505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5d43df9c11963e4b0e365e779e63981833ea41bdcc5d4db11c675fcc84fab3`  
		Last Modified: Sat, 19 Mar 2022 00:54:06 GMT  
		Size: 2.8 MB (2781278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad002987a7bae850089e45777bc9a362a9f8e3c656bdbbb26980ec4776d4704b`  
		Last Modified: Sat, 19 Mar 2022 00:54:05 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f6d4797a5cc96449c367b48271ff6c2fdb6908b35b0b9c4c548113d8535a9`  
		Last Modified: Sat, 19 Mar 2022 17:50:44 GMT  
		Size: 1.4 MB (1383662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cde83364d3aeeba3311efa235a8b37ae7bbe49fd46d82e326c8c363b094c82`  
		Last Modified: Sat, 19 Mar 2022 17:50:46 GMT  
		Size: 9.6 MB (9568502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be81ef1a0fd0acf9499a994c1da09ef250cbadcbc2faaeccd4bf84af6fda4956`  
		Last Modified: Tue, 22 Mar 2022 09:49:17 GMT  
		Size: 74.3 MB (74262518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c707d1882e7a22e27458c5bc3dab90eded7fce83699e2ba619cfaa97617bb07`  
		Last Modified: Tue, 22 Mar 2022 09:49:02 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40` - linux; ppc64le

```console
$ docker pull ghost@sha256:e01cb2e12a3c0c6642d370fb6a62d94ef478d4d1984db86324228cc57edbd4ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155582038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8168e6014a1fff905f12c4432217b0ce1b9397f135365a5fcd4691868f7ae152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:54:03 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:06:48 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:11:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:11:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:14:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:14:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:14:53 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:46:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:47:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:47:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:47:55 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:49:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:49:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:49:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:42 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:54:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:55:01 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:55:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:55:04 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:55:09 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:55:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca53b81b04fce4349fb7d53e6c96231409ea54bc6d07808c393a268d8fcd78c3`  
		Last Modified: Fri, 18 Mar 2022 08:33:21 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307e188a803758441743ab6c2c16c58d32cd25920f05e601d9fa75c13f8ec1f4`  
		Last Modified: Sat, 19 Mar 2022 02:15:29 GMT  
		Size: 38.0 MB (37978420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a74008e734f41eb1091af470bca5677108b1eb61729b017bd6e96944fc1c1`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 2.8 MB (2782569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c9e81db75711e347d46105e0daee9e64692433ad3141a1cf1a52bca316993e`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d14ae585ca54d978c72b25f6580d1c2986a60f049aefed6a7146e58b8eb07da`  
		Last Modified: Sun, 20 Mar 2022 00:12:26 GMT  
		Size: 1.4 MB (1367834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4904132a0f018373255a9418743ef13604d402190eaf4737c0de15b28964951`  
		Last Modified: Sun, 20 Mar 2022 00:12:31 GMT  
		Size: 9.6 MB (9568608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f2ab968cb74f11279d0c7784eac2069dae1dd4e24e911ca465976b7508ea9e`  
		Last Modified: Tue, 22 Mar 2022 01:56:01 GMT  
		Size: 68.6 MB (68599661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231cbb386dec32edcb41b2680932b86df8d092267a1cc20cd8460d53e2de5fa1`  
		Last Modified: Tue, 22 Mar 2022 01:55:43 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40` - linux; s390x

```console
$ docker pull ghost@sha256:fe87a6607cc14c1e6d541b390418e86d94ef0e6a2f1a5824ce2a34be28dd42fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147374040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7785b0540fceae7764559a39b1b6c6d004271adb765c9c7d1bf0a450eec91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:50:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:14:52 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:15:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:15:12 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:15:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:15:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:15:22 GMT
CMD ["node"]
# Sat, 19 Mar 2022 04:38:44 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 04:38:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 04:38:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 04:38:53 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 04:39:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 04:41:25 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 04:44:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 04:44:34 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 04:44:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 04:44:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 04:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 04:44:35 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 04:44:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722821cfaf9b99e01207f42d38caa8d0eea9818925d58a5d590057ff6271525d`  
		Last Modified: Thu, 17 Mar 2022 14:21:32 GMT  
		Size: 4.2 KB (4189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8924acd2003e404035ae30769a9ed0531c116ccfe4965f354999da4c593b38dc`  
		Last Modified: Fri, 18 Mar 2022 23:10:07 GMT  
		Size: 35.9 MB (35913738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c92724e1dbac9baa9b4949197499bd94e7abda3f1392dd48cc6f78fb23589`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 2.8 MB (2782997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f42e3d4bc22c450816fb2255b83b884ec091394d12aff4a84c65c1193e935a`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a61fd10dbc4124b4be87498e57bca3e89cab9d50ed7acf9934d6103e2b32eb`  
		Last Modified: Sat, 19 Mar 2022 04:42:48 GMT  
		Size: 1.4 MB (1434956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d6f9332f2c9557e6d14acdf3a51fb916f10fa41d64027309df97ce26b51dbc`  
		Last Modified: Sat, 19 Mar 2022 04:42:49 GMT  
		Size: 9.6 MB (9567431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb15d072ea322a0984e1bc07bc2080dbb63a6377aacd148ea5a7e6bb2ef70ab3`  
		Last Modified: Tue, 22 Mar 2022 04:45:09 GMT  
		Size: 68.0 MB (68013938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74647066b08d262304545c5cd408b3e338c2ba369d364130b19402b25f9787c`  
		Last Modified: Tue, 22 Mar 2022 04:44:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.40-alpine`

```console
$ docker pull ghost@sha256:6fbb449ae5780a8b11233638f905ae05de86aa353e6873d1b314bedf24d323ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4.40-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:a77e68ccf7dda2ee3792ddbe7410b135017da73587a3b92f2551a2151d3f9a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120273400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae8c19cb15f05412656942201f77c420d714951fc8fdb4e26842fdc91da84e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 21:48:35 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:48:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 21:48:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:48:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 21:48:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:48:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:48:56 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:07:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 00:07:07 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 00:07:07 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:07:07 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:07:34 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:20:40 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:21:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:21:49 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:21:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:21:49 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:21:49 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:21:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580248b309d4fecaf2f75f42a36796a166140238395d38d36e0d47b20dded70`  
		Last Modified: Fri, 18 Mar 2022 22:13:15 GMT  
		Size: 37.1 MB (37132855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539902d50a314143ea1ff8b98bee2aae6a9e66b7f102cd5b0ba0b3b21650132e`  
		Last Modified: Fri, 18 Mar 2022 22:13:07 GMT  
		Size: 2.4 MB (2358489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d60032af439ffa29833ceee54906865bfc7e32949f8a0643d3e1f7307d6e`  
		Last Modified: Fri, 18 Mar 2022 22:13:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d799310e8353a5bf7d35c0a576c8cc8a22f423a2268da6c937e55e512240daf`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87a58ecffcb615b1c9af4968b84fdfb44fd7f432d7d7c6087a14f7ba7f201e`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 816.9 KB (816859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf689cb927dd935805d71b57cb514cc956df63b009fc1453a79c668d2dad985d`  
		Last Modified: Sat, 19 Mar 2022 00:10:04 GMT  
		Size: 9.6 MB (9567883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ba8f128db30b568c1afb77c95580ad9ea781beedbf02c8e710cf6f5cef54`  
		Last Modified: Tue, 22 Mar 2022 01:22:57 GMT  
		Size: 67.6 MB (67568935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ccf55d8c338f0b82f1e2891980a21d7c3c6bd2459b3c5bb230c58d7c3abfa`  
		Last Modified: Tue, 22 Mar 2022 01:22:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:6eb1dcf99ed6f26af1b845ee6be822a8792ef60012e9f4c6e1b4d66048067c09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121481209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04611e77a27d6228f5b1763798b34668030f2fd913d3c6fd909a9b20bab8415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 19:31:23 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 19:47:55 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 19:47:56 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 19:48:04 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 19:48:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 19:48:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 19:48:06 GMT
CMD ["node"]
# Fri, 18 Mar 2022 21:05:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 18 Mar 2022 21:05:06 GMT
RUN apk add --no-cache 		bash
# Fri, 18 Mar 2022 21:05:06 GMT
ENV NODE_ENV=production
# Fri, 18 Mar 2022 21:05:06 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Fri, 18 Mar 2022 21:06:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 18 Mar 2022 21:06:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 18 Mar 2022 21:06:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:49:29 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 00:58:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 00:58:30 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 00:58:30 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 00:58:31 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 00:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 00:58:32 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 00:58:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd48496521270c1ba2c1d855bd715f617b59d6498e2e407b804b566b7678087`  
		Last Modified: Fri, 18 Mar 2022 20:47:14 GMT  
		Size: 36.2 MB (36198526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5599fde36163c1ebda1ad804a5b327cc1609b46263a91060b9fc3a835d328be9`  
		Last Modified: Fri, 18 Mar 2022 20:47:01 GMT  
		Size: 2.4 MB (2418192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18709050207fe0cf4803ac4f14090c67a8729cd62b866e31ae708d3b6e7b9166`  
		Last Modified: Fri, 18 Mar 2022 20:46:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af606d946314fedea65ebbae67cbd1cecf6a786558facb4b88f3f5739e15c45b`  
		Last Modified: Fri, 18 Mar 2022 21:17:09 GMT  
		Size: 11.0 KB (10977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0954b81f1ae01a7d7b8339d694eef033a3a078ca6a23c44e8934eb1c6229c0`  
		Last Modified: Fri, 18 Mar 2022 21:17:10 GMT  
		Size: 771.0 KB (770953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455c516cdd5fda37a751a4a4b7ef0e58ecb18b7c3fb786fb1f485daa97406bee`  
		Last Modified: Fri, 18 Mar 2022 21:17:19 GMT  
		Size: 9.6 MB (9569616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c7fbc400c37ccd72196b5ce76baac59ecf3caac1ffed927371e017585928ab`  
		Last Modified: Tue, 22 Mar 2022 01:00:33 GMT  
		Size: 69.9 MB (69882585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee202258538a801abcb089b73edb50aedd95524c1ea3bb6e48507e0e12cff5`  
		Last Modified: Tue, 22 Mar 2022 00:59:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:0644cf2d840856b3b3b40294c669e01ddcc682aea78116a58f4411bd42e64a74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a949fc5edc87eb366eafe3542807d0cce220766ee5d07bde46387085a173034`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 22:22:50 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:36:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 22:36:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:36:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 22:36:17 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:36:18 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:32:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 23:32:12 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 23:32:13 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:32:13 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:33:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:33:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:33:07 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:05:44 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:12:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:12:57 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:12:58 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:12:58 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:12:59 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:12:59 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7fb7593e1ec2c0060c773dbbf85fcbe77df0a45cbc891cd7f775442f959ce6`  
		Last Modified: Sat, 19 Mar 2022 00:04:50 GMT  
		Size: 35.8 MB (35750941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b531d0f3fa4a8c1e5c8c32c0c6a9de8cda1e078ed43db62853858f7ef792044b`  
		Last Modified: Sat, 19 Mar 2022 00:04:27 GMT  
		Size: 2.4 MB (2418360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ead18221dfbeb2afd1c7044892b00c01b6b056d5feb01c74684dff97d67e8eb`  
		Last Modified: Sat, 19 Mar 2022 00:04:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1faeeef23a40a6e07406285a95e3f94a86314cef806a54bbf3e2672288624dc`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 10.8 KB (10772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41729cace1ddd94023eba72c5c881b17ee1ab0e939be1d113c4f144fdae876c1`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 703.9 KB (703890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca1f8edf6ec39144c3fa34019e53bf9892978c935ab4b45e035f61c9cd7e32b`  
		Last Modified: Sat, 19 Mar 2022 23:42:57 GMT  
		Size: 9.6 MB (9569052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da276e29c5e8450fa177e6d44587e3deaf6cfd77e57b31dc25d000b5f5ccfd`  
		Last Modified: Tue, 22 Mar 2022 01:16:33 GMT  
		Size: 69.4 MB (69352758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee60ff28d8cf519c5f76cf745628e7c194ebe3f1ba8c04ad29aa550de0d86f`  
		Last Modified: Tue, 22 Mar 2022 01:15:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c3acf9a8c79217eac40fc9d89cec24c52d29d2831b2d2e8face8145b35bdff92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139988964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56691249b0321d0f36da40f17d7967c308221441d74557bf9032398ab19dbb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 23:07:29 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:28:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 23:28:15 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:28:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 23:28:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:28:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:28:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:45:45 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 17:45:47 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 17:45:47 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:45:48 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:46:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:46:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:46:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:44:48 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:48:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:48:24 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:48:27 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:48:29 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 09:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:48:34 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:48:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c992e90d8c9f9d1552190d2c0c3fa8fb5e94e39970cd9453e2819dc8b40ec1`  
		Last Modified: Sat, 19 Mar 2022 00:52:52 GMT  
		Size: 37.0 MB (37013909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc77e26b629b7d5ec72075b9db80763d03618483ac484e3129801b1b8131c6fe`  
		Last Modified: Sat, 19 Mar 2022 00:52:45 GMT  
		Size: 2.4 MB (2425472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36be0e7c4d5b1efb3a4be2317e16421a2d536fefec860c776192b0e5447a112`  
		Last Modified: Sat, 19 Mar 2022 00:52:44 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f881f7c1a27e3be051f3f7a6dc8e2234929511ade4258d41308f3b54ac77285`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ed0c2707cfd63880efce177bce0dc0dcb620859f33f8eb2c8661ad10a49e5`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 826.0 KB (826035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b3448e3e9cafa84aaabc148a2d7dff4a9270250a65345e20bf35c1c76c37`  
		Last Modified: Sat, 19 Mar 2022 17:51:19 GMT  
		Size: 9.6 MB (9567877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58636e87905f213f67950f1595df76af6261b3839115ec785486bdc81be9aed`  
		Last Modified: Tue, 22 Mar 2022 09:49:51 GMT  
		Size: 87.4 MB (87427790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be17ef9ec12b78c3e972aca3d3acfd1718fa34340d87ebadf1cb2a111bee70`  
		Last Modified: Tue, 22 Mar 2022 09:49:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.40.0`

```console
$ docker pull ghost@sha256:8f5f8956bf0507cc4e1d1fd97bd0a40dcdad36e27330055cb3355a683e74692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.40.0` - linux; amd64

```console
$ docker pull ghost@sha256:40009e56de3db4de60243e1e62c8f16fb49b00b3d5a7a0770b857dcf7b8aab45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148139873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce6a785b302d09270261554593de0515b71ecb032d9845d74c0fc5fd7ca2fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 13:00:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 21:50:00 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:50:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 21:50:35 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:50:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 21:50:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:50:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:50:47 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:04:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 00:04:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 00:04:43 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:04:44 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:05:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:32 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:20:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:20:37 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:20:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:20:37 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:20:37 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:20:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bc29d3bc64ca0852101d86667b4a0d1908f05fe0bfead140cf838c0be01bc3`  
		Last Modified: Thu, 17 Mar 2022 13:19:15 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a71a1d6cc6986624592a148f866355b9b90ddcd4a1f24be36b0f849d8c1044`  
		Last Modified: Fri, 18 Mar 2022 22:14:33 GMT  
		Size: 36.0 MB (36048047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5afd073302f60aad2c5067b89a976a5572fa262d0b60478970f307f8f94b97`  
		Last Modified: Fri, 18 Mar 2022 22:14:27 GMT  
		Size: 2.8 MB (2781848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5878f59eaa39846dd1173083e2e77dc140082be0efc61f7838c3403c6254b113`  
		Last Modified: Fri, 18 Mar 2022 22:14:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753aec878444f5bbf5b9e13544f6a3caf78aae1d01d506806f4b342c32623f2a`  
		Last Modified: Sat, 19 Mar 2022 00:09:27 GMT  
		Size: 1.4 MB (1448123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e282a0a274714713330c2ae37bb9aa1be203226d7ffd7de6eec07f2e35270c8`  
		Last Modified: Sat, 19 Mar 2022 00:09:31 GMT  
		Size: 9.6 MB (9567975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba50ac34f7d063eb291142ba6663fa92b6fa22f83af83d6ac81c45a985edf82`  
		Last Modified: Tue, 22 Mar 2022 01:22:28 GMT  
		Size: 66.9 MB (66912128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca556e8b36141f67594a9dc845b46b3d4f7f97af03cce35b90ab4bb48617284`  
		Last Modified: Tue, 22 Mar 2022 01:22:16 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:496e4906ab53cce4e3b11a603a6c690e04041a35f041feef37984a85905c0f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146919839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51074a20029823e0c80fbcdf0fba912ccb81421e46b76785c731b7eb26e987e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:47:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:50:57 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:51:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:51:48 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:52:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:52:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:52:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:52:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:22:42 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:23:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:23:10 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:23:10 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:23:59 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:57:33 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:05:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:05:28 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:05:29 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:05:29 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:05:30 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:05:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c69f71c16ec3df2b7d124845d1b3b6e6495150f4ea3398c32a390afffbf142`  
		Last Modified: Fri, 18 Mar 2022 17:06:49 GMT  
		Size: 4.2 KB (4166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b32ca858e17b62400e3e3939b76745bd091c2302dcb5a659f98f4036c58ad`  
		Last Modified: Sat, 19 Mar 2022 00:07:18 GMT  
		Size: 34.2 MB (34206692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2605fefc93565569e993984be795855508fc11258205a2f0ab736807a40c2c`  
		Last Modified: Sat, 19 Mar 2022 00:06:56 GMT  
		Size: 2.8 MB (2772408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649abf5b9f938b138570d940f0d8c3af7d265d4e26a25cf69fbd121df9381c`  
		Last Modified: Sat, 19 Mar 2022 00:06:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4041d8d2d15b52a58284107ec1fbc633900cce1fc07418607ed52ea1564428aa`  
		Last Modified: Sat, 19 Mar 2022 23:41:13 GMT  
		Size: 1.4 MB (1400322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04c308287b4673d9ba168fbb3d4cec8b9c7e8a9fe4ce8e8bab11f7a83658e18`  
		Last Modified: Sat, 19 Mar 2022 23:41:27 GMT  
		Size: 9.6 MB (9569190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af17b4d49e748753d815dd39cf5821fd799c9661f0abaf3b1647d224609fe020`  
		Last Modified: Tue, 22 Mar 2022 01:15:00 GMT  
		Size: 72.4 MB (72390962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092670288c46febff531959fa7f27513c2ca9c780ae8bbcfd90945b263032b6`  
		Last Modified: Tue, 22 Mar 2022 01:13:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ff551f487def98ff5a1f560a93046cc5ac2c95df28cc70f7cd6d88f631cc266
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154218519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c0be74ec3768fb3421c9b9c6a2b4d1d12d2a3e7e0002cd920f5d572ac544f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:20:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:50:24 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:50:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:50:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:51:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:51:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:51:04 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:41:23 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 17:41:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:41:34 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:41:35 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:42:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:42:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:41:06 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:44:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:44:18 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:44:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:44:23 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 09:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:44:28 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:44:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e302ce9f0603b4af265c90ba2a4807900c24096808fb68bf44300bd440542`  
		Last Modified: Thu, 17 Mar 2022 13:54:35 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98badb25d325c02976fab44804955d995b60a19fc609da8e3f1e642c52d898f9`  
		Last Modified: Sat, 19 Mar 2022 00:54:11 GMT  
		Size: 36.2 MB (36154505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5d43df9c11963e4b0e365e779e63981833ea41bdcc5d4db11c675fcc84fab3`  
		Last Modified: Sat, 19 Mar 2022 00:54:06 GMT  
		Size: 2.8 MB (2781278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad002987a7bae850089e45777bc9a362a9f8e3c656bdbbb26980ec4776d4704b`  
		Last Modified: Sat, 19 Mar 2022 00:54:05 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f6d4797a5cc96449c367b48271ff6c2fdb6908b35b0b9c4c548113d8535a9`  
		Last Modified: Sat, 19 Mar 2022 17:50:44 GMT  
		Size: 1.4 MB (1383662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cde83364d3aeeba3311efa235a8b37ae7bbe49fd46d82e326c8c363b094c82`  
		Last Modified: Sat, 19 Mar 2022 17:50:46 GMT  
		Size: 9.6 MB (9568502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be81ef1a0fd0acf9499a994c1da09ef250cbadcbc2faaeccd4bf84af6fda4956`  
		Last Modified: Tue, 22 Mar 2022 09:49:17 GMT  
		Size: 74.3 MB (74262518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c707d1882e7a22e27458c5bc3dab90eded7fce83699e2ba619cfaa97617bb07`  
		Last Modified: Tue, 22 Mar 2022 09:49:02 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:e01cb2e12a3c0c6642d370fb6a62d94ef478d4d1984db86324228cc57edbd4ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155582038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8168e6014a1fff905f12c4432217b0ce1b9397f135365a5fcd4691868f7ae152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:54:03 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:06:48 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:11:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:11:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:14:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:14:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:14:53 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:46:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:47:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:47:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:47:55 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:49:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:49:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:49:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:42 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:54:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:55:01 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:55:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:55:04 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:55:09 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:55:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca53b81b04fce4349fb7d53e6c96231409ea54bc6d07808c393a268d8fcd78c3`  
		Last Modified: Fri, 18 Mar 2022 08:33:21 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307e188a803758441743ab6c2c16c58d32cd25920f05e601d9fa75c13f8ec1f4`  
		Last Modified: Sat, 19 Mar 2022 02:15:29 GMT  
		Size: 38.0 MB (37978420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a74008e734f41eb1091af470bca5677108b1eb61729b017bd6e96944fc1c1`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 2.8 MB (2782569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c9e81db75711e347d46105e0daee9e64692433ad3141a1cf1a52bca316993e`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d14ae585ca54d978c72b25f6580d1c2986a60f049aefed6a7146e58b8eb07da`  
		Last Modified: Sun, 20 Mar 2022 00:12:26 GMT  
		Size: 1.4 MB (1367834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4904132a0f018373255a9418743ef13604d402190eaf4737c0de15b28964951`  
		Last Modified: Sun, 20 Mar 2022 00:12:31 GMT  
		Size: 9.6 MB (9568608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f2ab968cb74f11279d0c7784eac2069dae1dd4e24e911ca465976b7508ea9e`  
		Last Modified: Tue, 22 Mar 2022 01:56:01 GMT  
		Size: 68.6 MB (68599661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231cbb386dec32edcb41b2680932b86df8d092267a1cc20cd8460d53e2de5fa1`  
		Last Modified: Tue, 22 Mar 2022 01:55:43 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0` - linux; s390x

```console
$ docker pull ghost@sha256:fe87a6607cc14c1e6d541b390418e86d94ef0e6a2f1a5824ce2a34be28dd42fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147374040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7785b0540fceae7764559a39b1b6c6d004271adb765c9c7d1bf0a450eec91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:50:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:14:52 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:15:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:15:12 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:15:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:15:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:15:22 GMT
CMD ["node"]
# Sat, 19 Mar 2022 04:38:44 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 04:38:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 04:38:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 04:38:53 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 04:39:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 04:41:25 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 04:44:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 04:44:34 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 04:44:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 04:44:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 04:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 04:44:35 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 04:44:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722821cfaf9b99e01207f42d38caa8d0eea9818925d58a5d590057ff6271525d`  
		Last Modified: Thu, 17 Mar 2022 14:21:32 GMT  
		Size: 4.2 KB (4189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8924acd2003e404035ae30769a9ed0531c116ccfe4965f354999da4c593b38dc`  
		Last Modified: Fri, 18 Mar 2022 23:10:07 GMT  
		Size: 35.9 MB (35913738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c92724e1dbac9baa9b4949197499bd94e7abda3f1392dd48cc6f78fb23589`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 2.8 MB (2782997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f42e3d4bc22c450816fb2255b83b884ec091394d12aff4a84c65c1193e935a`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a61fd10dbc4124b4be87498e57bca3e89cab9d50ed7acf9934d6103e2b32eb`  
		Last Modified: Sat, 19 Mar 2022 04:42:48 GMT  
		Size: 1.4 MB (1434956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d6f9332f2c9557e6d14acdf3a51fb916f10fa41d64027309df97ce26b51dbc`  
		Last Modified: Sat, 19 Mar 2022 04:42:49 GMT  
		Size: 9.6 MB (9567431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb15d072ea322a0984e1bc07bc2080dbb63a6377aacd148ea5a7e6bb2ef70ab3`  
		Last Modified: Tue, 22 Mar 2022 04:45:09 GMT  
		Size: 68.0 MB (68013938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74647066b08d262304545c5cd408b3e338c2ba369d364130b19402b25f9787c`  
		Last Modified: Tue, 22 Mar 2022 04:44:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.40.0-alpine`

```console
$ docker pull ghost@sha256:6fbb449ae5780a8b11233638f905ae05de86aa353e6873d1b314bedf24d323ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4.40.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:a77e68ccf7dda2ee3792ddbe7410b135017da73587a3b92f2551a2151d3f9a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120273400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae8c19cb15f05412656942201f77c420d714951fc8fdb4e26842fdc91da84e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 21:48:35 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:48:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 21:48:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:48:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 21:48:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:48:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:48:56 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:07:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 00:07:07 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 00:07:07 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:07:07 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:07:34 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:20:40 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:21:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:21:49 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:21:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:21:49 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:21:49 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:21:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580248b309d4fecaf2f75f42a36796a166140238395d38d36e0d47b20dded70`  
		Last Modified: Fri, 18 Mar 2022 22:13:15 GMT  
		Size: 37.1 MB (37132855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539902d50a314143ea1ff8b98bee2aae6a9e66b7f102cd5b0ba0b3b21650132e`  
		Last Modified: Fri, 18 Mar 2022 22:13:07 GMT  
		Size: 2.4 MB (2358489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d60032af439ffa29833ceee54906865bfc7e32949f8a0643d3e1f7307d6e`  
		Last Modified: Fri, 18 Mar 2022 22:13:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d799310e8353a5bf7d35c0a576c8cc8a22f423a2268da6c937e55e512240daf`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87a58ecffcb615b1c9af4968b84fdfb44fd7f432d7d7c6087a14f7ba7f201e`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 816.9 KB (816859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf689cb927dd935805d71b57cb514cc956df63b009fc1453a79c668d2dad985d`  
		Last Modified: Sat, 19 Mar 2022 00:10:04 GMT  
		Size: 9.6 MB (9567883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ba8f128db30b568c1afb77c95580ad9ea781beedbf02c8e710cf6f5cef54`  
		Last Modified: Tue, 22 Mar 2022 01:22:57 GMT  
		Size: 67.6 MB (67568935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ccf55d8c338f0b82f1e2891980a21d7c3c6bd2459b3c5bb230c58d7c3abfa`  
		Last Modified: Tue, 22 Mar 2022 01:22:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:6eb1dcf99ed6f26af1b845ee6be822a8792ef60012e9f4c6e1b4d66048067c09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121481209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04611e77a27d6228f5b1763798b34668030f2fd913d3c6fd909a9b20bab8415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 19:31:23 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 19:47:55 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 19:47:56 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 19:48:04 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 19:48:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 19:48:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 19:48:06 GMT
CMD ["node"]
# Fri, 18 Mar 2022 21:05:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 18 Mar 2022 21:05:06 GMT
RUN apk add --no-cache 		bash
# Fri, 18 Mar 2022 21:05:06 GMT
ENV NODE_ENV=production
# Fri, 18 Mar 2022 21:05:06 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Fri, 18 Mar 2022 21:06:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 18 Mar 2022 21:06:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 18 Mar 2022 21:06:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:49:29 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 00:58:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 00:58:30 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 00:58:30 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 00:58:31 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 00:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 00:58:32 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 00:58:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd48496521270c1ba2c1d855bd715f617b59d6498e2e407b804b566b7678087`  
		Last Modified: Fri, 18 Mar 2022 20:47:14 GMT  
		Size: 36.2 MB (36198526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5599fde36163c1ebda1ad804a5b327cc1609b46263a91060b9fc3a835d328be9`  
		Last Modified: Fri, 18 Mar 2022 20:47:01 GMT  
		Size: 2.4 MB (2418192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18709050207fe0cf4803ac4f14090c67a8729cd62b866e31ae708d3b6e7b9166`  
		Last Modified: Fri, 18 Mar 2022 20:46:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af606d946314fedea65ebbae67cbd1cecf6a786558facb4b88f3f5739e15c45b`  
		Last Modified: Fri, 18 Mar 2022 21:17:09 GMT  
		Size: 11.0 KB (10977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0954b81f1ae01a7d7b8339d694eef033a3a078ca6a23c44e8934eb1c6229c0`  
		Last Modified: Fri, 18 Mar 2022 21:17:10 GMT  
		Size: 771.0 KB (770953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455c516cdd5fda37a751a4a4b7ef0e58ecb18b7c3fb786fb1f485daa97406bee`  
		Last Modified: Fri, 18 Mar 2022 21:17:19 GMT  
		Size: 9.6 MB (9569616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c7fbc400c37ccd72196b5ce76baac59ecf3caac1ffed927371e017585928ab`  
		Last Modified: Tue, 22 Mar 2022 01:00:33 GMT  
		Size: 69.9 MB (69882585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee202258538a801abcb089b73edb50aedd95524c1ea3bb6e48507e0e12cff5`  
		Last Modified: Tue, 22 Mar 2022 00:59:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:0644cf2d840856b3b3b40294c669e01ddcc682aea78116a58f4411bd42e64a74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a949fc5edc87eb366eafe3542807d0cce220766ee5d07bde46387085a173034`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 22:22:50 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:36:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 22:36:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:36:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 22:36:17 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:36:18 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:32:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 23:32:12 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 23:32:13 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:32:13 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:33:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:33:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:33:07 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:05:44 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:12:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:12:57 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:12:58 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:12:58 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:12:59 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:12:59 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7fb7593e1ec2c0060c773dbbf85fcbe77df0a45cbc891cd7f775442f959ce6`  
		Last Modified: Sat, 19 Mar 2022 00:04:50 GMT  
		Size: 35.8 MB (35750941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b531d0f3fa4a8c1e5c8c32c0c6a9de8cda1e078ed43db62853858f7ef792044b`  
		Last Modified: Sat, 19 Mar 2022 00:04:27 GMT  
		Size: 2.4 MB (2418360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ead18221dfbeb2afd1c7044892b00c01b6b056d5feb01c74684dff97d67e8eb`  
		Last Modified: Sat, 19 Mar 2022 00:04:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1faeeef23a40a6e07406285a95e3f94a86314cef806a54bbf3e2672288624dc`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 10.8 KB (10772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41729cace1ddd94023eba72c5c881b17ee1ab0e939be1d113c4f144fdae876c1`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 703.9 KB (703890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca1f8edf6ec39144c3fa34019e53bf9892978c935ab4b45e035f61c9cd7e32b`  
		Last Modified: Sat, 19 Mar 2022 23:42:57 GMT  
		Size: 9.6 MB (9569052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da276e29c5e8450fa177e6d44587e3deaf6cfd77e57b31dc25d000b5f5ccfd`  
		Last Modified: Tue, 22 Mar 2022 01:16:33 GMT  
		Size: 69.4 MB (69352758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee60ff28d8cf519c5f76cf745628e7c194ebe3f1ba8c04ad29aa550de0d86f`  
		Last Modified: Tue, 22 Mar 2022 01:15:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.40.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c3acf9a8c79217eac40fc9d89cec24c52d29d2831b2d2e8face8145b35bdff92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139988964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56691249b0321d0f36da40f17d7967c308221441d74557bf9032398ab19dbb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 23:07:29 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:28:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 23:28:15 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:28:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 23:28:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:28:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:28:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:45:45 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 17:45:47 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 17:45:47 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:45:48 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:46:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:46:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:46:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:44:48 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:48:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:48:24 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:48:27 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:48:29 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 09:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:48:34 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:48:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c992e90d8c9f9d1552190d2c0c3fa8fb5e94e39970cd9453e2819dc8b40ec1`  
		Last Modified: Sat, 19 Mar 2022 00:52:52 GMT  
		Size: 37.0 MB (37013909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc77e26b629b7d5ec72075b9db80763d03618483ac484e3129801b1b8131c6fe`  
		Last Modified: Sat, 19 Mar 2022 00:52:45 GMT  
		Size: 2.4 MB (2425472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36be0e7c4d5b1efb3a4be2317e16421a2d536fefec860c776192b0e5447a112`  
		Last Modified: Sat, 19 Mar 2022 00:52:44 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f881f7c1a27e3be051f3f7a6dc8e2234929511ade4258d41308f3b54ac77285`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ed0c2707cfd63880efce177bce0dc0dcb620859f33f8eb2c8661ad10a49e5`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 826.0 KB (826035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b3448e3e9cafa84aaabc148a2d7dff4a9270250a65345e20bf35c1c76c37`  
		Last Modified: Sat, 19 Mar 2022 17:51:19 GMT  
		Size: 9.6 MB (9567877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58636e87905f213f67950f1595df76af6261b3839115ec785486bdc81be9aed`  
		Last Modified: Tue, 22 Mar 2022 09:49:51 GMT  
		Size: 87.4 MB (87427790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be17ef9ec12b78c3e972aca3d3acfd1718fa34340d87ebadf1cb2a111bee70`  
		Last Modified: Tue, 22 Mar 2022 09:49:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:6fbb449ae5780a8b11233638f905ae05de86aa353e6873d1b314bedf24d323ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:a77e68ccf7dda2ee3792ddbe7410b135017da73587a3b92f2551a2151d3f9a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120273400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae8c19cb15f05412656942201f77c420d714951fc8fdb4e26842fdc91da84e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 21:48:35 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:48:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 21:48:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:48:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 21:48:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:48:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:48:56 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:07:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 00:07:07 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 00:07:07 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:07:07 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:07:34 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:07:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:20:40 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:21:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:21:49 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:21:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:21:49 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:21:49 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:21:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580248b309d4fecaf2f75f42a36796a166140238395d38d36e0d47b20dded70`  
		Last Modified: Fri, 18 Mar 2022 22:13:15 GMT  
		Size: 37.1 MB (37132855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539902d50a314143ea1ff8b98bee2aae6a9e66b7f102cd5b0ba0b3b21650132e`  
		Last Modified: Fri, 18 Mar 2022 22:13:07 GMT  
		Size: 2.4 MB (2358489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d60032af439ffa29833ceee54906865bfc7e32949f8a0643d3e1f7307d6e`  
		Last Modified: Fri, 18 Mar 2022 22:13:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d799310e8353a5bf7d35c0a576c8cc8a22f423a2268da6c937e55e512240daf`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87a58ecffcb615b1c9af4968b84fdfb44fd7f432d7d7c6087a14f7ba7f201e`  
		Last Modified: Sat, 19 Mar 2022 00:10:01 GMT  
		Size: 816.9 KB (816859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf689cb927dd935805d71b57cb514cc956df63b009fc1453a79c668d2dad985d`  
		Last Modified: Sat, 19 Mar 2022 00:10:04 GMT  
		Size: 9.6 MB (9567883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ba8f128db30b568c1afb77c95580ad9ea781beedbf02c8e710cf6f5cef54`  
		Last Modified: Tue, 22 Mar 2022 01:22:57 GMT  
		Size: 67.6 MB (67568935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ccf55d8c338f0b82f1e2891980a21d7c3c6bd2459b3c5bb230c58d7c3abfa`  
		Last Modified: Tue, 22 Mar 2022 01:22:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:6eb1dcf99ed6f26af1b845ee6be822a8792ef60012e9f4c6e1b4d66048067c09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121481209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04611e77a27d6228f5b1763798b34668030f2fd913d3c6fd909a9b20bab8415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 19:31:23 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 19:47:55 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 19:47:56 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 19:48:04 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 19:48:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 19:48:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 19:48:06 GMT
CMD ["node"]
# Fri, 18 Mar 2022 21:05:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 18 Mar 2022 21:05:06 GMT
RUN apk add --no-cache 		bash
# Fri, 18 Mar 2022 21:05:06 GMT
ENV NODE_ENV=production
# Fri, 18 Mar 2022 21:05:06 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Fri, 18 Mar 2022 21:06:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 18 Mar 2022 21:06:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 18 Mar 2022 21:06:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:49:29 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 00:58:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 00:58:30 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 00:58:30 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 00:58:31 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 00:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 00:58:32 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 00:58:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd48496521270c1ba2c1d855bd715f617b59d6498e2e407b804b566b7678087`  
		Last Modified: Fri, 18 Mar 2022 20:47:14 GMT  
		Size: 36.2 MB (36198526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5599fde36163c1ebda1ad804a5b327cc1609b46263a91060b9fc3a835d328be9`  
		Last Modified: Fri, 18 Mar 2022 20:47:01 GMT  
		Size: 2.4 MB (2418192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18709050207fe0cf4803ac4f14090c67a8729cd62b866e31ae708d3b6e7b9166`  
		Last Modified: Fri, 18 Mar 2022 20:46:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af606d946314fedea65ebbae67cbd1cecf6a786558facb4b88f3f5739e15c45b`  
		Last Modified: Fri, 18 Mar 2022 21:17:09 GMT  
		Size: 11.0 KB (10977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0954b81f1ae01a7d7b8339d694eef033a3a078ca6a23c44e8934eb1c6229c0`  
		Last Modified: Fri, 18 Mar 2022 21:17:10 GMT  
		Size: 771.0 KB (770953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455c516cdd5fda37a751a4a4b7ef0e58ecb18b7c3fb786fb1f485daa97406bee`  
		Last Modified: Fri, 18 Mar 2022 21:17:19 GMT  
		Size: 9.6 MB (9569616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c7fbc400c37ccd72196b5ce76baac59ecf3caac1ffed927371e017585928ab`  
		Last Modified: Tue, 22 Mar 2022 01:00:33 GMT  
		Size: 69.9 MB (69882585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee202258538a801abcb089b73edb50aedd95524c1ea3bb6e48507e0e12cff5`  
		Last Modified: Tue, 22 Mar 2022 00:59:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:0644cf2d840856b3b3b40294c669e01ddcc682aea78116a58f4411bd42e64a74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a949fc5edc87eb366eafe3542807d0cce220766ee5d07bde46387085a173034`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 22:22:50 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:36:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 22:36:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:36:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 22:36:17 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:36:18 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:32:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 23:32:12 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 23:32:13 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:32:13 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:33:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:33:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:33:07 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:05:44 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:12:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:12:57 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:12:58 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:12:58 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 01:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:12:59 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:12:59 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7fb7593e1ec2c0060c773dbbf85fcbe77df0a45cbc891cd7f775442f959ce6`  
		Last Modified: Sat, 19 Mar 2022 00:04:50 GMT  
		Size: 35.8 MB (35750941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b531d0f3fa4a8c1e5c8c32c0c6a9de8cda1e078ed43db62853858f7ef792044b`  
		Last Modified: Sat, 19 Mar 2022 00:04:27 GMT  
		Size: 2.4 MB (2418360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ead18221dfbeb2afd1c7044892b00c01b6b056d5feb01c74684dff97d67e8eb`  
		Last Modified: Sat, 19 Mar 2022 00:04:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1faeeef23a40a6e07406285a95e3f94a86314cef806a54bbf3e2672288624dc`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 10.8 KB (10772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41729cace1ddd94023eba72c5c881b17ee1ab0e939be1d113c4f144fdae876c1`  
		Last Modified: Sat, 19 Mar 2022 23:42:42 GMT  
		Size: 703.9 KB (703890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca1f8edf6ec39144c3fa34019e53bf9892978c935ab4b45e035f61c9cd7e32b`  
		Last Modified: Sat, 19 Mar 2022 23:42:57 GMT  
		Size: 9.6 MB (9569052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da276e29c5e8450fa177e6d44587e3deaf6cfd77e57b31dc25d000b5f5ccfd`  
		Last Modified: Tue, 22 Mar 2022 01:16:33 GMT  
		Size: 69.4 MB (69352758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee60ff28d8cf519c5f76cf745628e7c194ebe3f1ba8c04ad29aa550de0d86f`  
		Last Modified: Tue, 22 Mar 2022 01:15:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c3acf9a8c79217eac40fc9d89cec24c52d29d2831b2d2e8face8145b35bdff92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139988964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56691249b0321d0f36da40f17d7967c308221441d74557bf9032398ab19dbb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 23:07:29 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:28:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 18 Mar 2022 23:28:15 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:28:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 18 Mar 2022 23:28:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:28:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:28:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:45:45 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 19 Mar 2022 17:45:47 GMT
RUN apk add --no-cache 		bash
# Sat, 19 Mar 2022 17:45:47 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:45:48 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:46:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:46:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:46:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:44:48 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:48:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:48:24 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:48:27 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:48:29 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 22 Mar 2022 09:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:48:34 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:48:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c992e90d8c9f9d1552190d2c0c3fa8fb5e94e39970cd9453e2819dc8b40ec1`  
		Last Modified: Sat, 19 Mar 2022 00:52:52 GMT  
		Size: 37.0 MB (37013909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc77e26b629b7d5ec72075b9db80763d03618483ac484e3129801b1b8131c6fe`  
		Last Modified: Sat, 19 Mar 2022 00:52:45 GMT  
		Size: 2.4 MB (2425472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36be0e7c4d5b1efb3a4be2317e16421a2d536fefec860c776192b0e5447a112`  
		Last Modified: Sat, 19 Mar 2022 00:52:44 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f881f7c1a27e3be051f3f7a6dc8e2234929511ade4258d41308f3b54ac77285`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ed0c2707cfd63880efce177bce0dc0dcb620859f33f8eb2c8661ad10a49e5`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 826.0 KB (826035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b3448e3e9cafa84aaabc148a2d7dff4a9270250a65345e20bf35c1c76c37`  
		Last Modified: Sat, 19 Mar 2022 17:51:19 GMT  
		Size: 9.6 MB (9567877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58636e87905f213f67950f1595df76af6261b3839115ec785486bdc81be9aed`  
		Last Modified: Tue, 22 Mar 2022 09:49:51 GMT  
		Size: 87.4 MB (87427790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be17ef9ec12b78c3e972aca3d3acfd1718fa34340d87ebadf1cb2a111bee70`  
		Last Modified: Tue, 22 Mar 2022 09:49:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:8f5f8956bf0507cc4e1d1fd97bd0a40dcdad36e27330055cb3355a683e74692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:40009e56de3db4de60243e1e62c8f16fb49b00b3d5a7a0770b857dcf7b8aab45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148139873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce6a785b302d09270261554593de0515b71ecb032d9845d74c0fc5fd7ca2fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 13:00:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 21:50:00 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 21:50:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 21:50:35 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 21:50:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 21:50:47 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:50:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:50:47 GMT
CMD ["node"]
# Sat, 19 Mar 2022 00:04:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 00:04:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 00:04:43 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 00:04:44 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 00:05:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:32 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:20:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:20:37 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:20:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:20:37 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:20:37 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:20:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bc29d3bc64ca0852101d86667b4a0d1908f05fe0bfead140cf838c0be01bc3`  
		Last Modified: Thu, 17 Mar 2022 13:19:15 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a71a1d6cc6986624592a148f866355b9b90ddcd4a1f24be36b0f849d8c1044`  
		Last Modified: Fri, 18 Mar 2022 22:14:33 GMT  
		Size: 36.0 MB (36048047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5afd073302f60aad2c5067b89a976a5572fa262d0b60478970f307f8f94b97`  
		Last Modified: Fri, 18 Mar 2022 22:14:27 GMT  
		Size: 2.8 MB (2781848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5878f59eaa39846dd1173083e2e77dc140082be0efc61f7838c3403c6254b113`  
		Last Modified: Fri, 18 Mar 2022 22:14:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753aec878444f5bbf5b9e13544f6a3caf78aae1d01d506806f4b342c32623f2a`  
		Last Modified: Sat, 19 Mar 2022 00:09:27 GMT  
		Size: 1.4 MB (1448123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e282a0a274714713330c2ae37bb9aa1be203226d7ffd7de6eec07f2e35270c8`  
		Last Modified: Sat, 19 Mar 2022 00:09:31 GMT  
		Size: 9.6 MB (9567975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba50ac34f7d063eb291142ba6663fa92b6fa22f83af83d6ac81c45a985edf82`  
		Last Modified: Tue, 22 Mar 2022 01:22:28 GMT  
		Size: 66.9 MB (66912128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca556e8b36141f67594a9dc845b46b3d4f7f97af03cce35b90ab4bb48617284`  
		Last Modified: Tue, 22 Mar 2022 01:22:16 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:496e4906ab53cce4e3b11a603a6c690e04041a35f041feef37984a85905c0f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146919839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51074a20029823e0c80fbcdf0fba912ccb81421e46b76785c731b7eb26e987e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:03 GMT
ADD file:e52f9ee2dc3144d7b9eb3ec90c106aa2a094eb4c5c2aa8cbff5c520a5faaef43 in / 
# Thu, 17 Mar 2022 09:31:04 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:47:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:50:57 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:51:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:51:48 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:52:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:52:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:52:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:52:23 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:22:42 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:23:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:23:10 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:23:10 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:23:59 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:24:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 00:57:33 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:05:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:05:28 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:05:29 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:05:29 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:05:30 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:05:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e5e708ee1f9fdbc69324391f7d1f816c657e6116eff09e7d2247fa9de3a076a`  
		Last Modified: Thu, 17 Mar 2022 09:46:33 GMT  
		Size: 26.6 MB (26575097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c69f71c16ec3df2b7d124845d1b3b6e6495150f4ea3398c32a390afffbf142`  
		Last Modified: Fri, 18 Mar 2022 17:06:49 GMT  
		Size: 4.2 KB (4166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b32ca858e17b62400e3e3939b76745bd091c2302dcb5a659f98f4036c58ad`  
		Last Modified: Sat, 19 Mar 2022 00:07:18 GMT  
		Size: 34.2 MB (34206692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2605fefc93565569e993984be795855508fc11258205a2f0ab736807a40c2c`  
		Last Modified: Sat, 19 Mar 2022 00:06:56 GMT  
		Size: 2.8 MB (2772408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649abf5b9f938b138570d940f0d8c3af7d265d4e26a25cf69fbd121df9381c`  
		Last Modified: Sat, 19 Mar 2022 00:06:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4041d8d2d15b52a58284107ec1fbc633900cce1fc07418607ed52ea1564428aa`  
		Last Modified: Sat, 19 Mar 2022 23:41:13 GMT  
		Size: 1.4 MB (1400322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04c308287b4673d9ba168fbb3d4cec8b9c7e8a9fe4ce8e8bab11f7a83658e18`  
		Last Modified: Sat, 19 Mar 2022 23:41:27 GMT  
		Size: 9.6 MB (9569190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af17b4d49e748753d815dd39cf5821fd799c9661f0abaf3b1647d224609fe020`  
		Last Modified: Tue, 22 Mar 2022 01:15:00 GMT  
		Size: 72.4 MB (72390962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092670288c46febff531959fa7f27513c2ca9c780ae8bbcfd90945b263032b6`  
		Last Modified: Tue, 22 Mar 2022 01:13:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9ff551f487def98ff5a1f560a93046cc5ac2c95df28cc70f7cd6d88f631cc266
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154218519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c0be74ec3768fb3421c9b9c6a2b4d1d12d2a3e7e0002cd920f5d572ac544f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:20:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:50:24 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:50:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:50:49 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:51:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:51:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:51:04 GMT
CMD ["node"]
# Sat, 19 Mar 2022 17:41:23 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 17:41:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:41:34 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 17:41:35 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 17:42:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 17:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 17:42:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 09:41:06 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 09:44:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 09:44:18 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 09:44:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 09:44:23 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 09:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 09:44:28 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 09:44:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e302ce9f0603b4af265c90ba2a4807900c24096808fb68bf44300bd440542`  
		Last Modified: Thu, 17 Mar 2022 13:54:35 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98badb25d325c02976fab44804955d995b60a19fc609da8e3f1e642c52d898f9`  
		Last Modified: Sat, 19 Mar 2022 00:54:11 GMT  
		Size: 36.2 MB (36154505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5d43df9c11963e4b0e365e779e63981833ea41bdcc5d4db11c675fcc84fab3`  
		Last Modified: Sat, 19 Mar 2022 00:54:06 GMT  
		Size: 2.8 MB (2781278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad002987a7bae850089e45777bc9a362a9f8e3c656bdbbb26980ec4776d4704b`  
		Last Modified: Sat, 19 Mar 2022 00:54:05 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f6d4797a5cc96449c367b48271ff6c2fdb6908b35b0b9c4c548113d8535a9`  
		Last Modified: Sat, 19 Mar 2022 17:50:44 GMT  
		Size: 1.4 MB (1383662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cde83364d3aeeba3311efa235a8b37ae7bbe49fd46d82e326c8c363b094c82`  
		Last Modified: Sat, 19 Mar 2022 17:50:46 GMT  
		Size: 9.6 MB (9568502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be81ef1a0fd0acf9499a994c1da09ef250cbadcbc2faaeccd4bf84af6fda4956`  
		Last Modified: Tue, 22 Mar 2022 09:49:17 GMT  
		Size: 74.3 MB (74262518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c707d1882e7a22e27458c5bc3dab90eded7fce83699e2ba619cfaa97617bb07`  
		Last Modified: Tue, 22 Mar 2022 09:49:02 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:e01cb2e12a3c0c6642d370fb6a62d94ef478d4d1984db86324228cc57edbd4ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155582038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8168e6014a1fff905f12c4432217b0ce1b9397f135365a5fcd4691868f7ae152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:54:03 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 23:06:48 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 23:11:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 23:11:09 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 23:14:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 23:14:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 23:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 23:14:53 GMT
CMD ["node"]
# Sat, 19 Mar 2022 23:46:25 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 23:47:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 23:47:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 23:47:55 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 23:49:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 23:49:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 23:49:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 01:19:42 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 01:54:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 01:55:01 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 01:55:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 01:55:04 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 01:55:09 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 01:55:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca53b81b04fce4349fb7d53e6c96231409ea54bc6d07808c393a268d8fcd78c3`  
		Last Modified: Fri, 18 Mar 2022 08:33:21 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307e188a803758441743ab6c2c16c58d32cd25920f05e601d9fa75c13f8ec1f4`  
		Last Modified: Sat, 19 Mar 2022 02:15:29 GMT  
		Size: 38.0 MB (37978420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a74008e734f41eb1091af470bca5677108b1eb61729b017bd6e96944fc1c1`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 2.8 MB (2782569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c9e81db75711e347d46105e0daee9e64692433ad3141a1cf1a52bca316993e`  
		Last Modified: Sat, 19 Mar 2022 02:15:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d14ae585ca54d978c72b25f6580d1c2986a60f049aefed6a7146e58b8eb07da`  
		Last Modified: Sun, 20 Mar 2022 00:12:26 GMT  
		Size: 1.4 MB (1367834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4904132a0f018373255a9418743ef13604d402190eaf4737c0de15b28964951`  
		Last Modified: Sun, 20 Mar 2022 00:12:31 GMT  
		Size: 9.6 MB (9568608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f2ab968cb74f11279d0c7784eac2069dae1dd4e24e911ca465976b7508ea9e`  
		Last Modified: Tue, 22 Mar 2022 01:56:01 GMT  
		Size: 68.6 MB (68599661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231cbb386dec32edcb41b2680932b86df8d092267a1cc20cd8460d53e2de5fa1`  
		Last Modified: Tue, 22 Mar 2022 01:55:43 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:fe87a6607cc14c1e6d541b390418e86d94ef0e6a2f1a5824ce2a34be28dd42fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147374040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7785b0540fceae7764559a39b1b6c6d004271adb765c9c7d1bf0a450eec91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 12:50:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 18 Mar 2022 22:14:52 GMT
ENV NODE_VERSION=14.19.1
# Fri, 18 Mar 2022 22:15:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 18 Mar 2022 22:15:12 GMT
ENV YARN_VERSION=1.22.17
# Fri, 18 Mar 2022 22:15:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 18 Mar 2022 22:15:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 18 Mar 2022 22:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 22:15:22 GMT
CMD ["node"]
# Sat, 19 Mar 2022 04:38:44 GMT
ENV GOSU_VERSION=1.12
# Sat, 19 Mar 2022 04:38:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 04:38:53 GMT
ENV NODE_ENV=production
# Sat, 19 Mar 2022 04:38:53 GMT
ENV GHOST_CLI_VERSION=1.18.2
# Sat, 19 Mar 2022 04:39:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 19 Mar 2022 04:39:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 22 Mar 2022 04:41:25 GMT
ENV GHOST_VERSION=4.40.0
# Tue, 22 Mar 2022 04:44:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 22 Mar 2022 04:44:34 GMT
WORKDIR /var/lib/ghost
# Tue, 22 Mar 2022 04:44:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 22 Mar 2022 04:44:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 22 Mar 2022 04:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Mar 2022 04:44:35 GMT
EXPOSE 2368
# Tue, 22 Mar 2022 04:44:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722821cfaf9b99e01207f42d38caa8d0eea9818925d58a5d590057ff6271525d`  
		Last Modified: Thu, 17 Mar 2022 14:21:32 GMT  
		Size: 4.2 KB (4189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8924acd2003e404035ae30769a9ed0531c116ccfe4965f354999da4c593b38dc`  
		Last Modified: Fri, 18 Mar 2022 23:10:07 GMT  
		Size: 35.9 MB (35913738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c92724e1dbac9baa9b4949197499bd94e7abda3f1392dd48cc6f78fb23589`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 2.8 MB (2782997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f42e3d4bc22c450816fb2255b83b884ec091394d12aff4a84c65c1193e935a`  
		Last Modified: Fri, 18 Mar 2022 23:10:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a61fd10dbc4124b4be87498e57bca3e89cab9d50ed7acf9934d6103e2b32eb`  
		Last Modified: Sat, 19 Mar 2022 04:42:48 GMT  
		Size: 1.4 MB (1434956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d6f9332f2c9557e6d14acdf3a51fb916f10fa41d64027309df97ce26b51dbc`  
		Last Modified: Sat, 19 Mar 2022 04:42:49 GMT  
		Size: 9.6 MB (9567431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb15d072ea322a0984e1bc07bc2080dbb63a6377aacd148ea5a7e6bb2ef70ab3`  
		Last Modified: Tue, 22 Mar 2022 04:45:09 GMT  
		Size: 68.0 MB (68013938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74647066b08d262304545c5cd408b3e338c2ba369d364130b19402b25f9787c`  
		Last Modified: Tue, 22 Mar 2022 04:44:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

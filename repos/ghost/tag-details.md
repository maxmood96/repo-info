<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:4`](#ghost4)
-	[`ghost:4-alpine`](#ghost4-alpine)
-	[`ghost:4.48`](#ghost448)
-	[`ghost:4.48-alpine`](#ghost448-alpine)
-	[`ghost:4.48.7`](#ghost4487)
-	[`ghost:4.48.7-alpine`](#ghost4487-alpine)
-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.22`](#ghost522)
-	[`ghost:5.22-alpine`](#ghost522-alpine)
-	[`ghost:5.22.10`](#ghost52210)
-	[`ghost:5.22.10-alpine`](#ghost52210-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:4`

```console
$ docker pull ghost@sha256:238d171dd5573e65d11ec1d15ce270ebf884b6029eb10387530222e3548e5814
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
$ docker pull ghost@sha256:68a5e602f66c84446aef747c11d0f81c35a5477c613a7bf4334ed48566e9781b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166263198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678f31e8b765746566749c4bd0cc5174d4889cb09d4f86cff04ffc47475073cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:25:19 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 13:25:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:25:42 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:25:54 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:25:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:25:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:25:55 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:32:06 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:32:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:32:17 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:32:17 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:32:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:32:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:32:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:32:45 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 23:34:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:34:17 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:34:17 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:34:17 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:34:17 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:34:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee12449a27b6cbefe837194d05282d4d28e9981b266f7f8945e0d10c5c081a0`  
		Last Modified: Tue, 15 Nov 2022 13:35:07 GMT  
		Size: 36.5 MB (36540040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90525a6fb0ebfcbd8cdb96903e3c52bccd7e7c57b7de3762924add0ba881945`  
		Last Modified: Tue, 15 Nov 2022 13:35:02 GMT  
		Size: 2.8 MB (2781637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23472a292ea8b8c6819caa310dddcc37b2b4539c444cb9983a04f6e006da09f2`  
		Last Modified: Tue, 15 Nov 2022 13:35:01 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ba2ab5cac3209b0a549ed2497636850d29fe11cd9d0cbbce5183d8f7768a8`  
		Last Modified: Tue, 15 Nov 2022 23:35:21 GMT  
		Size: 1.4 MB (1449325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596e6441777f22456d37b914015b835ec65bdf33ea364d1132c02ebd89473b3`  
		Last Modified: Tue, 15 Nov 2022 23:35:24 GMT  
		Size: 10.2 MB (10245518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0452f0dff034e8385fd87d6ff37c881007ca59792002145dc620168cfd35f34e`  
		Last Modified: Tue, 15 Nov 2022 23:35:37 GMT  
		Size: 83.8 MB (83828866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5aeb94ccb633a866500c4fc408a1f572ae6ddc9198a78c585c0376ab19f78a`  
		Last Modified: Tue, 15 Nov 2022 23:35:21 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm variant v7

```console
$ docker pull ghost@sha256:de14351be64a36c8c0fed48887d7775be51f9a97d5726451c16395e3495396a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180009241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629fb91d7fdf2a0df9b71224ac9a93875de4fa89e081a46a45363f89cae0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 01:12:50 GMT
ENV NODE_VERSION=14.21.1
# Wed, 09 Nov 2022 01:13:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 01:13:13 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 01:13:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 01:13:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 01:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 01:13:26 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:51:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:51:15 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:51:15 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:51:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_VERSION=4.48.7
# Wed, 09 Nov 2022 02:55:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 09 Nov 2022 02:55:55 GMT
WORKDIR /var/lib/ghost
# Wed, 09 Nov 2022 02:55:55 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 09 Nov 2022 02:55:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 09 Nov 2022 02:55:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 02:55:55 GMT
EXPOSE 2368
# Wed, 09 Nov 2022 02:55:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e93103f5a562c6a7250ddc25cfe8dff94860a97ea989f067abb9ae43d9f0c`  
		Last Modified: Wed, 09 Nov 2022 01:35:08 GMT  
		Size: 34.7 MB (34697192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91059937fcb19bb229f85b3c4bb581bc39f1b80528f4ea6bb167877811cb9181`  
		Last Modified: Wed, 09 Nov 2022 01:35:02 GMT  
		Size: 2.8 MB (2770997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9131d4652683ee7acf70dfabd07742f285353018aa436deab01cfde598d6655`  
		Last Modified: Wed, 09 Nov 2022 01:35:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904cef64f1f319bd7d8a9331083fb767b9f15761360a0f276d5d3e3d32237d12`  
		Last Modified: Wed, 09 Nov 2022 03:03:32 GMT  
		Size: 1.4 MB (1401984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71552646e26dd5c1e76eb87e66e29d408d28604b9c9ef8173585a77b1c8cb414`  
		Last Modified: Wed, 09 Nov 2022 03:03:36 GMT  
		Size: 10.2 MB (10244479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4241375b5255913ac27d83be6312c3414222e300954fa5c5e82b40fe5f4059f2`  
		Last Modified: Wed, 09 Nov 2022 03:04:01 GMT  
		Size: 104.3 MB (104310150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6d6594be7958beddfb2e49e3220814b8807288d08a3d291e19975a698459f4`  
		Last Modified: Wed, 09 Nov 2022 03:03:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:970f96f6b6e59e56760b9f0494e6a5042b22c0c0f1562c219f0699ca1a84f167
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162675660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc47c581375a83a56f6bc01b2b99ac158cef444e12fdc9adc585472e8dc3e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:47:54 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 06:48:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:48:14 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:48:24 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:48:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:48:24 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:18:58 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:19:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:19:07 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:19:07 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:19:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 22:20:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:20:52 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:20:52 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:20:52 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:20:52 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:20:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527a0b13fec73f848ad1b714b457491ce3ba72ddec974c5a6675bc8407fff72`  
		Last Modified: Tue, 15 Nov 2022 06:57:33 GMT  
		Size: 36.7 MB (36650706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c9297d2b26b9b0f1ec86282b9ffd0dd96345dacf0dfb9bbc45257e26ae9e4e`  
		Last Modified: Tue, 15 Nov 2022 06:57:29 GMT  
		Size: 2.8 MB (2781406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39660e2b870dc1d2f360412bc304537113d0f5d983af67635d0c7b68150a2951`  
		Last Modified: Tue, 15 Nov 2022 06:57:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7313de62eabfe7302f0a8406f13f473d8b3b9b2a427b4152691a0f8c0425ab50`  
		Last Modified: Tue, 15 Nov 2022 22:21:56 GMT  
		Size: 1.4 MB (1385216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2a95c963f5a587458f5eb1850d80cc0d1e44d5ba1dd1cb58355814b78eea7a`  
		Last Modified: Tue, 15 Nov 2022 22:21:58 GMT  
		Size: 10.2 MB (10245217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34de58bc6111651c393c9437497741489fae4eb5e450040072c21f3791497538`  
		Last Modified: Tue, 15 Nov 2022 22:22:09 GMT  
		Size: 81.5 MB (81547332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf86a8fe1dc94d1ad71b0fd6a833a8713f1392ae95845b15668136f90bf1bb5`  
		Last Modified: Tue, 15 Nov 2022 22:21:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; ppc64le

```console
$ docker pull ghost@sha256:472108e72a9f8b7acc492222caf5f786a930445541e3fa997667e023d5e9c722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179485761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696ea1ae277858971dda69656400ecd1354bba2cb4af681fe5133a568eada427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:10:01 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 18:10:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:10:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:11:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:11:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:11:11 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:27:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:27:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:27:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:27:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:28:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 19:36:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:37:06 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:37:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:37:07 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:37:09 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:37:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280fd52e4db435fcfbd4455998ab6b003a18dd9c81667a19e4932662d1b6d23`  
		Last Modified: Tue, 15 Nov 2022 18:21:04 GMT  
		Size: 38.5 MB (38465872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2810c606a78bf1e5de3f9bd19ebc774867cdfb5cd664b77fa05f40a988a5d8be`  
		Last Modified: Tue, 15 Nov 2022 18:20:55 GMT  
		Size: 2.8 MB (2781533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c7cb0647ab1994480257ba0718c71cec8235dbb7b6c6ea3b13ec601efabfc`  
		Last Modified: Tue, 15 Nov 2022 18:20:54 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb544f8f9262f08664b3cb6a8dbadf395832983093416f34742c0237532b76d`  
		Last Modified: Tue, 15 Nov 2022 19:38:47 GMT  
		Size: 1.4 MB (1369041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa1da6b1ecc386866a81422b350eb365fff97858ad90a64e0cf950d4826dad`  
		Last Modified: Tue, 15 Nov 2022 19:38:52 GMT  
		Size: 10.2 MB (10245733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d05097413d17963f366e8b00a52c591d70ea06dd70c892a31afd3e8e0c16a17`  
		Last Modified: Tue, 15 Nov 2022 19:39:21 GMT  
		Size: 91.3 MB (91333264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcff9c647fc44136b0a623cae47edf0cadcbeff19e8e9f89557918c550023b2`  
		Last Modified: Tue, 15 Nov 2022 19:38:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; s390x

```console
$ docker pull ghost@sha256:39c0136ef28c1012eca95f7941f55c36e768fea34de2c6b22321a960a471e90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171267829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66794ea866fbed5d851c0a50533ec3bd396d890166b98dbfc348dd316ab76351`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:13:33 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 08:14:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:14:27 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:14:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:14:57 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:14:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:14:58 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:21:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:21:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:21:44 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:21:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:22:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:22:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:22:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:22:48 GMT
ENV GHOST_VERSION=4.48.7
# Wed, 16 Nov 2022 01:35:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:35:52 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:35:53 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:35:53 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:35:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:35:54 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:35:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669536de4c4a877c9ba64dea9a85cb2082decdef35f73674dae78c727a09b286`  
		Last Modified: Tue, 15 Nov 2022 08:23:06 GMT  
		Size: 36.4 MB (36407040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7640ec25984afbdb2a21ba06f2bad09dd9d32018133b8fed325615f9709005e`  
		Last Modified: Tue, 15 Nov 2022 08:23:02 GMT  
		Size: 2.8 MB (2784207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5265e89340cb1ee22fa6df2f166f26abeb1d324bd1c9b50867d01557ac5fab28`  
		Last Modified: Tue, 15 Nov 2022 08:23:01 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ff8a26c0e98944b7aa11f47161560bda78ab1a2e0d348b6a4796de17da7aac`  
		Last Modified: Wed, 16 Nov 2022 01:36:55 GMT  
		Size: 1.4 MB (1436325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204491b21c117e8e97183d92778f5ceb48cb63f57e6c0202c99b544d6ff22c2`  
		Last Modified: Wed, 16 Nov 2022 01:36:57 GMT  
		Size: 10.2 MB (10245601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ce9194dd83160c5de6b20bac633cb8d0a4e43fe4f7856fe9c87cada7b5ce0`  
		Last Modified: Wed, 16 Nov 2022 01:37:11 GMT  
		Size: 90.7 MB (90745687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c706a7bd2e6cf3713b984afce47b02b2a20d0a8785d5cca3963056fe200a0188`  
		Last Modified: Wed, 16 Nov 2022 01:36:54 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4-alpine`

```console
$ docker pull ghost@sha256:3cb4e563b6c8f96fd5f19aeae32a19892bf34e71c56f83f45953f7479d69f766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4da829f81b6fed3d63296fb4d33e5593a2ecb9e3fcfc8a45c18ffff44c82a5c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138529046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f590d33bc1954519265b3e6845d64c446521ba4988e742b01f58cca69086747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:32:07 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 06:32:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:32:16 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:32:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:32:20 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:32:20 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:27:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:27:36 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:27:36 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:27:36 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 11:28:01 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 11:29:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 11:29:39 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 11:29:39 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 11:29:40 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 11:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:29:40 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 11:29:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c774934c91f00c542a1fb93212d42cf819d47de47169f00eba8db7e7026f51`  
		Last Modified: Sat, 12 Nov 2022 06:37:20 GMT  
		Size: 37.7 MB (37724346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d9211bf297cc0df2b07d2ad8ee5a83f5f479165228a1a513004dba925cfc20`  
		Last Modified: Sat, 12 Nov 2022 06:37:15 GMT  
		Size: 2.4 MB (2368725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14523e6c1be223f204f3266fd2d66cc5d9caf28f41364bfa565923c09ed3b4db`  
		Last Modified: Sat, 12 Nov 2022 06:37:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6df5a33c8d055ce1259d2b29b7854405e699e1b444b523db9b1bf8342f9fc26`  
		Last Modified: Sat, 12 Nov 2022 11:30:32 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cf5c4a5c5408e30aa38cc30b22c9d22699130f32b2537db3e4ef7316ad003`  
		Last Modified: Sat, 12 Nov 2022 11:30:32 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5fa079d29a8020c2f30554dec49ebf6b4f476258dfcd337a6dd3d7e982384`  
		Last Modified: Sat, 12 Nov 2022 11:30:35 GMT  
		Size: 10.2 MB (10245542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3922449be4564a3926b8b3bf9782d9773df8f0472787745a4e72f69111cd2dc5`  
		Last Modified: Sat, 12 Nov 2022 11:30:48 GMT  
		Size: 84.6 MB (84551804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7770868a814ace688266d135c566d8caa4e4e0380a8f185e670df92dd721e21c`  
		Last Modified: Sat, 12 Nov 2022 11:30:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:610087d2d38d72249bb2282bb5a7aa1c3f5d67a1c7b434a076b6869de6e89190
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142193449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced480230185dbe29a7675ff123e589acc9f220b5be61090060f623eb7ece52f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 10:49:14 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 11:23:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 11:23:48 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 11:23:54 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 11:23:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 11:23:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:23:55 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:15:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:15:58 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:15:58 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:15:58 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:16:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 14:22:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 14:22:23 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 14:22:23 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 14:22:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 14:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 14:22:23 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 14:22:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2013ca6af2177095883e23da431551e40beacbe9b328bd9a64b101c7afb7af44`  
		Last Modified: Sat, 12 Nov 2022 11:29:32 GMT  
		Size: 36.7 MB (36749486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206761edc1c09db4001f2e6e0ec7451ce3e09df10209b08330620e64ac1a5ba4`  
		Last Modified: Sat, 12 Nov 2022 11:29:25 GMT  
		Size: 2.4 MB (2417570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b20dd6b1b095cad4cf131f991c687c89721cc3b787ad3f134c76b75472b8d9`  
		Last Modified: Sat, 12 Nov 2022 11:29:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0af623f089836b4d1c0948bdf9f60e6d9b0cb1cb213e3b91310aabc839fd16`  
		Last Modified: Sat, 12 Nov 2022 14:23:48 GMT  
		Size: 11.0 KB (10992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f949fa7d5d18587a9c4c5bd0ecf584329557957f7f2c2ef1a8c2a292e8112a72`  
		Last Modified: Sat, 12 Nov 2022 14:23:49 GMT  
		Size: 772.0 KB (771958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddc36407495dd1762664fbc5aa936ce3a4ab1dd65adebc12a2a166c5e01a64`  
		Last Modified: Sat, 12 Nov 2022 14:23:53 GMT  
		Size: 10.2 MB (10245693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d200752754072d904b9125051ec21f3ea13656be04575118afbe4763ccf301`  
		Last Modified: Sat, 12 Nov 2022 14:24:16 GMT  
		Size: 89.4 MB (89381646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910bc20053c92e69bbb19f3c7fd368ded5cf3982e1f234fe2fca6ec74ae0f8e`  
		Last Modified: Sat, 12 Nov 2022 14:23:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:590a7e1deda42fac6d1c0d281bb9ce87efb6ca3fcc7d6bcbee6bb4b7b363f378
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140913490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84065f533f3be0eb91c61d85585cba048f95b021a05244044a88027bfeaed95a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 12:29:08 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 12:49:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:49:24 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:49:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:49:29 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:49:29 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:10:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:10:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:10:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:10:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:10:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:10:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:10:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 19:10:54 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 19:15:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 19:15:21 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 19:15:21 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 19:15:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 19:15:21 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 19:15:21 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b251d39d15356abea2c79230cf242fab87ea74bcd05dd281e6f94fe97e36e4`  
		Last Modified: Sat, 12 Nov 2022 13:00:48 GMT  
		Size: 36.7 MB (36669594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a1a3e393e3b1bfc92d8653ae53a13c82581b6e927af79f7fa56cd75be265ee`  
		Last Modified: Sat, 12 Nov 2022 13:00:42 GMT  
		Size: 2.4 MB (2417705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cc7093a86ad8a89189e7286dfaaf1a732af19710a95ccc4e194c4e27fe80d8`  
		Last Modified: Sat, 12 Nov 2022 13:00:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eee7557e1106e8660cb2248f22e7a56393c67a6af0267619d9d0947e1dd68bd`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77eda6ad1a4963332eab5f01c258f2803d646f5c4b51d4831d3f396881e27e3`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 704.7 KB (704668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f04ca0a1d999700ebaa7f545e48615c0e834cc567695bca2b323052456127`  
		Last Modified: Sat, 12 Nov 2022 19:17:11 GMT  
		Size: 10.2 MB (10245678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a252b6d2d21633078745f922be7f3fbfb481def9319386ce4ac9e4fa2c54d3df`  
		Last Modified: Sat, 12 Nov 2022 19:17:34 GMT  
		Size: 88.4 MB (88445261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581a5d260656a2cf7c5a32efebbf847d7fbc8cb7a80a0db0b84aa5e6aed2ee28`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:109488734bec69a8f3a9e3a0d74b8df485083868929b5035a5098023619dc9ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135469564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34104b1dc4517c3d5722e07442f52a0368dfbd2c69d0b9ec598d7158d0552ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:56:53 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 08:11:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 08:11:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 08:11:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 08:11:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:11:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:33:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:33:51 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:33:51 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:33:51 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:34:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 11:35:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 11:35:37 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 11:35:37 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 11:35:37 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 11:35:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:35:37 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 11:35:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3f8016cbc63b3b13a298021c1681bf77749b18a9aeaf756c4d57fee9c1c72`  
		Last Modified: Sat, 12 Nov 2022 08:16:07 GMT  
		Size: 37.6 MB (37552542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789bf1647f9802940b12385260daf689771a255e5c7508874b89e3f92abd4bb`  
		Last Modified: Sat, 12 Nov 2022 08:16:03 GMT  
		Size: 2.4 MB (2425934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9f9da8b41400f1fccb3ce147e7508de0fcba2852569735aa225e7b75c98926`  
		Last Modified: Sat, 12 Nov 2022 08:16:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccbb9dc2c54dcdda274ba33cfbe3fc7919c007ab182ebe828f4a45537812cba`  
		Last Modified: Sat, 12 Nov 2022 11:36:32 GMT  
		Size: 11.1 KB (11106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609e2bb235cf901848338bf5a92bc34385f1449e2c7391d125aa348f68f121d`  
		Last Modified: Sat, 12 Nov 2022 11:36:33 GMT  
		Size: 826.3 KB (826327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b1bf97318ed9deb56c6e49a57b09ea59ad67b9bbdbba05607f8e1e348a6a2`  
		Last Modified: Sat, 12 Nov 2022 11:36:35 GMT  
		Size: 10.2 MB (10245237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd5659d555ce60351f4c2b9cdd879e16fc28499569d06240b9c2ece09f77f2`  
		Last Modified: Sat, 12 Nov 2022 11:36:45 GMT  
		Size: 81.7 MB (81699667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4d9e96b34cc176e524724e1a668b723e4ef272039b568ca961e9c423746419`  
		Last Modified: Sat, 12 Nov 2022 11:36:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.48`

```console
$ docker pull ghost@sha256:238d171dd5573e65d11ec1d15ce270ebf884b6029eb10387530222e3548e5814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.48` - linux; amd64

```console
$ docker pull ghost@sha256:68a5e602f66c84446aef747c11d0f81c35a5477c613a7bf4334ed48566e9781b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166263198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678f31e8b765746566749c4bd0cc5174d4889cb09d4f86cff04ffc47475073cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:25:19 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 13:25:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:25:42 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:25:54 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:25:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:25:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:25:55 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:32:06 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:32:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:32:17 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:32:17 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:32:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:32:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:32:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:32:45 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 23:34:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:34:17 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:34:17 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:34:17 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:34:17 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:34:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee12449a27b6cbefe837194d05282d4d28e9981b266f7f8945e0d10c5c081a0`  
		Last Modified: Tue, 15 Nov 2022 13:35:07 GMT  
		Size: 36.5 MB (36540040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90525a6fb0ebfcbd8cdb96903e3c52bccd7e7c57b7de3762924add0ba881945`  
		Last Modified: Tue, 15 Nov 2022 13:35:02 GMT  
		Size: 2.8 MB (2781637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23472a292ea8b8c6819caa310dddcc37b2b4539c444cb9983a04f6e006da09f2`  
		Last Modified: Tue, 15 Nov 2022 13:35:01 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ba2ab5cac3209b0a549ed2497636850d29fe11cd9d0cbbce5183d8f7768a8`  
		Last Modified: Tue, 15 Nov 2022 23:35:21 GMT  
		Size: 1.4 MB (1449325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596e6441777f22456d37b914015b835ec65bdf33ea364d1132c02ebd89473b3`  
		Last Modified: Tue, 15 Nov 2022 23:35:24 GMT  
		Size: 10.2 MB (10245518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0452f0dff034e8385fd87d6ff37c881007ca59792002145dc620168cfd35f34e`  
		Last Modified: Tue, 15 Nov 2022 23:35:37 GMT  
		Size: 83.8 MB (83828866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5aeb94ccb633a866500c4fc408a1f572ae6ddc9198a78c585c0376ab19f78a`  
		Last Modified: Tue, 15 Nov 2022 23:35:21 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48` - linux; arm variant v7

```console
$ docker pull ghost@sha256:de14351be64a36c8c0fed48887d7775be51f9a97d5726451c16395e3495396a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180009241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629fb91d7fdf2a0df9b71224ac9a93875de4fa89e081a46a45363f89cae0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 01:12:50 GMT
ENV NODE_VERSION=14.21.1
# Wed, 09 Nov 2022 01:13:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 01:13:13 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 01:13:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 01:13:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 01:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 01:13:26 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:51:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:51:15 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:51:15 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:51:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_VERSION=4.48.7
# Wed, 09 Nov 2022 02:55:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 09 Nov 2022 02:55:55 GMT
WORKDIR /var/lib/ghost
# Wed, 09 Nov 2022 02:55:55 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 09 Nov 2022 02:55:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 09 Nov 2022 02:55:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 02:55:55 GMT
EXPOSE 2368
# Wed, 09 Nov 2022 02:55:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e93103f5a562c6a7250ddc25cfe8dff94860a97ea989f067abb9ae43d9f0c`  
		Last Modified: Wed, 09 Nov 2022 01:35:08 GMT  
		Size: 34.7 MB (34697192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91059937fcb19bb229f85b3c4bb581bc39f1b80528f4ea6bb167877811cb9181`  
		Last Modified: Wed, 09 Nov 2022 01:35:02 GMT  
		Size: 2.8 MB (2770997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9131d4652683ee7acf70dfabd07742f285353018aa436deab01cfde598d6655`  
		Last Modified: Wed, 09 Nov 2022 01:35:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904cef64f1f319bd7d8a9331083fb767b9f15761360a0f276d5d3e3d32237d12`  
		Last Modified: Wed, 09 Nov 2022 03:03:32 GMT  
		Size: 1.4 MB (1401984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71552646e26dd5c1e76eb87e66e29d408d28604b9c9ef8173585a77b1c8cb414`  
		Last Modified: Wed, 09 Nov 2022 03:03:36 GMT  
		Size: 10.2 MB (10244479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4241375b5255913ac27d83be6312c3414222e300954fa5c5e82b40fe5f4059f2`  
		Last Modified: Wed, 09 Nov 2022 03:04:01 GMT  
		Size: 104.3 MB (104310150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6d6594be7958beddfb2e49e3220814b8807288d08a3d291e19975a698459f4`  
		Last Modified: Wed, 09 Nov 2022 03:03:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:970f96f6b6e59e56760b9f0494e6a5042b22c0c0f1562c219f0699ca1a84f167
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162675660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc47c581375a83a56f6bc01b2b99ac158cef444e12fdc9adc585472e8dc3e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:47:54 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 06:48:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:48:14 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:48:24 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:48:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:48:24 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:18:58 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:19:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:19:07 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:19:07 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:19:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 22:20:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:20:52 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:20:52 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:20:52 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:20:52 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:20:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527a0b13fec73f848ad1b714b457491ce3ba72ddec974c5a6675bc8407fff72`  
		Last Modified: Tue, 15 Nov 2022 06:57:33 GMT  
		Size: 36.7 MB (36650706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c9297d2b26b9b0f1ec86282b9ffd0dd96345dacf0dfb9bbc45257e26ae9e4e`  
		Last Modified: Tue, 15 Nov 2022 06:57:29 GMT  
		Size: 2.8 MB (2781406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39660e2b870dc1d2f360412bc304537113d0f5d983af67635d0c7b68150a2951`  
		Last Modified: Tue, 15 Nov 2022 06:57:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7313de62eabfe7302f0a8406f13f473d8b3b9b2a427b4152691a0f8c0425ab50`  
		Last Modified: Tue, 15 Nov 2022 22:21:56 GMT  
		Size: 1.4 MB (1385216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2a95c963f5a587458f5eb1850d80cc0d1e44d5ba1dd1cb58355814b78eea7a`  
		Last Modified: Tue, 15 Nov 2022 22:21:58 GMT  
		Size: 10.2 MB (10245217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34de58bc6111651c393c9437497741489fae4eb5e450040072c21f3791497538`  
		Last Modified: Tue, 15 Nov 2022 22:22:09 GMT  
		Size: 81.5 MB (81547332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf86a8fe1dc94d1ad71b0fd6a833a8713f1392ae95845b15668136f90bf1bb5`  
		Last Modified: Tue, 15 Nov 2022 22:21:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48` - linux; ppc64le

```console
$ docker pull ghost@sha256:472108e72a9f8b7acc492222caf5f786a930445541e3fa997667e023d5e9c722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179485761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696ea1ae277858971dda69656400ecd1354bba2cb4af681fe5133a568eada427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:10:01 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 18:10:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:10:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:11:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:11:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:11:11 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:27:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:27:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:27:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:27:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:28:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 19:36:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:37:06 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:37:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:37:07 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:37:09 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:37:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280fd52e4db435fcfbd4455998ab6b003a18dd9c81667a19e4932662d1b6d23`  
		Last Modified: Tue, 15 Nov 2022 18:21:04 GMT  
		Size: 38.5 MB (38465872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2810c606a78bf1e5de3f9bd19ebc774867cdfb5cd664b77fa05f40a988a5d8be`  
		Last Modified: Tue, 15 Nov 2022 18:20:55 GMT  
		Size: 2.8 MB (2781533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c7cb0647ab1994480257ba0718c71cec8235dbb7b6c6ea3b13ec601efabfc`  
		Last Modified: Tue, 15 Nov 2022 18:20:54 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb544f8f9262f08664b3cb6a8dbadf395832983093416f34742c0237532b76d`  
		Last Modified: Tue, 15 Nov 2022 19:38:47 GMT  
		Size: 1.4 MB (1369041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa1da6b1ecc386866a81422b350eb365fff97858ad90a64e0cf950d4826dad`  
		Last Modified: Tue, 15 Nov 2022 19:38:52 GMT  
		Size: 10.2 MB (10245733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d05097413d17963f366e8b00a52c591d70ea06dd70c892a31afd3e8e0c16a17`  
		Last Modified: Tue, 15 Nov 2022 19:39:21 GMT  
		Size: 91.3 MB (91333264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcff9c647fc44136b0a623cae47edf0cadcbeff19e8e9f89557918c550023b2`  
		Last Modified: Tue, 15 Nov 2022 19:38:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48` - linux; s390x

```console
$ docker pull ghost@sha256:39c0136ef28c1012eca95f7941f55c36e768fea34de2c6b22321a960a471e90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171267829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66794ea866fbed5d851c0a50533ec3bd396d890166b98dbfc348dd316ab76351`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:13:33 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 08:14:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:14:27 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:14:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:14:57 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:14:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:14:58 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:21:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:21:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:21:44 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:21:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:22:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:22:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:22:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:22:48 GMT
ENV GHOST_VERSION=4.48.7
# Wed, 16 Nov 2022 01:35:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:35:52 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:35:53 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:35:53 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:35:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:35:54 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:35:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669536de4c4a877c9ba64dea9a85cb2082decdef35f73674dae78c727a09b286`  
		Last Modified: Tue, 15 Nov 2022 08:23:06 GMT  
		Size: 36.4 MB (36407040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7640ec25984afbdb2a21ba06f2bad09dd9d32018133b8fed325615f9709005e`  
		Last Modified: Tue, 15 Nov 2022 08:23:02 GMT  
		Size: 2.8 MB (2784207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5265e89340cb1ee22fa6df2f166f26abeb1d324bd1c9b50867d01557ac5fab28`  
		Last Modified: Tue, 15 Nov 2022 08:23:01 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ff8a26c0e98944b7aa11f47161560bda78ab1a2e0d348b6a4796de17da7aac`  
		Last Modified: Wed, 16 Nov 2022 01:36:55 GMT  
		Size: 1.4 MB (1436325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204491b21c117e8e97183d92778f5ceb48cb63f57e6c0202c99b544d6ff22c2`  
		Last Modified: Wed, 16 Nov 2022 01:36:57 GMT  
		Size: 10.2 MB (10245601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ce9194dd83160c5de6b20bac633cb8d0a4e43fe4f7856fe9c87cada7b5ce0`  
		Last Modified: Wed, 16 Nov 2022 01:37:11 GMT  
		Size: 90.7 MB (90745687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c706a7bd2e6cf3713b984afce47b02b2a20d0a8785d5cca3963056fe200a0188`  
		Last Modified: Wed, 16 Nov 2022 01:36:54 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.48-alpine`

```console
$ docker pull ghost@sha256:3cb4e563b6c8f96fd5f19aeae32a19892bf34e71c56f83f45953f7479d69f766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4.48-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4da829f81b6fed3d63296fb4d33e5593a2ecb9e3fcfc8a45c18ffff44c82a5c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138529046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f590d33bc1954519265b3e6845d64c446521ba4988e742b01f58cca69086747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:32:07 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 06:32:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:32:16 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:32:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:32:20 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:32:20 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:27:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:27:36 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:27:36 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:27:36 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 11:28:01 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 11:29:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 11:29:39 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 11:29:39 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 11:29:40 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 11:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:29:40 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 11:29:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c774934c91f00c542a1fb93212d42cf819d47de47169f00eba8db7e7026f51`  
		Last Modified: Sat, 12 Nov 2022 06:37:20 GMT  
		Size: 37.7 MB (37724346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d9211bf297cc0df2b07d2ad8ee5a83f5f479165228a1a513004dba925cfc20`  
		Last Modified: Sat, 12 Nov 2022 06:37:15 GMT  
		Size: 2.4 MB (2368725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14523e6c1be223f204f3266fd2d66cc5d9caf28f41364bfa565923c09ed3b4db`  
		Last Modified: Sat, 12 Nov 2022 06:37:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6df5a33c8d055ce1259d2b29b7854405e699e1b444b523db9b1bf8342f9fc26`  
		Last Modified: Sat, 12 Nov 2022 11:30:32 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cf5c4a5c5408e30aa38cc30b22c9d22699130f32b2537db3e4ef7316ad003`  
		Last Modified: Sat, 12 Nov 2022 11:30:32 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5fa079d29a8020c2f30554dec49ebf6b4f476258dfcd337a6dd3d7e982384`  
		Last Modified: Sat, 12 Nov 2022 11:30:35 GMT  
		Size: 10.2 MB (10245542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3922449be4564a3926b8b3bf9782d9773df8f0472787745a4e72f69111cd2dc5`  
		Last Modified: Sat, 12 Nov 2022 11:30:48 GMT  
		Size: 84.6 MB (84551804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7770868a814ace688266d135c566d8caa4e4e0380a8f185e670df92dd721e21c`  
		Last Modified: Sat, 12 Nov 2022 11:30:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:610087d2d38d72249bb2282bb5a7aa1c3f5d67a1c7b434a076b6869de6e89190
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142193449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced480230185dbe29a7675ff123e589acc9f220b5be61090060f623eb7ece52f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 10:49:14 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 11:23:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 11:23:48 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 11:23:54 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 11:23:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 11:23:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:23:55 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:15:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:15:58 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:15:58 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:15:58 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:16:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 14:22:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 14:22:23 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 14:22:23 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 14:22:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 14:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 14:22:23 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 14:22:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2013ca6af2177095883e23da431551e40beacbe9b328bd9a64b101c7afb7af44`  
		Last Modified: Sat, 12 Nov 2022 11:29:32 GMT  
		Size: 36.7 MB (36749486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206761edc1c09db4001f2e6e0ec7451ce3e09df10209b08330620e64ac1a5ba4`  
		Last Modified: Sat, 12 Nov 2022 11:29:25 GMT  
		Size: 2.4 MB (2417570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b20dd6b1b095cad4cf131f991c687c89721cc3b787ad3f134c76b75472b8d9`  
		Last Modified: Sat, 12 Nov 2022 11:29:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0af623f089836b4d1c0948bdf9f60e6d9b0cb1cb213e3b91310aabc839fd16`  
		Last Modified: Sat, 12 Nov 2022 14:23:48 GMT  
		Size: 11.0 KB (10992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f949fa7d5d18587a9c4c5bd0ecf584329557957f7f2c2ef1a8c2a292e8112a72`  
		Last Modified: Sat, 12 Nov 2022 14:23:49 GMT  
		Size: 772.0 KB (771958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddc36407495dd1762664fbc5aa936ce3a4ab1dd65adebc12a2a166c5e01a64`  
		Last Modified: Sat, 12 Nov 2022 14:23:53 GMT  
		Size: 10.2 MB (10245693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d200752754072d904b9125051ec21f3ea13656be04575118afbe4763ccf301`  
		Last Modified: Sat, 12 Nov 2022 14:24:16 GMT  
		Size: 89.4 MB (89381646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910bc20053c92e69bbb19f3c7fd368ded5cf3982e1f234fe2fca6ec74ae0f8e`  
		Last Modified: Sat, 12 Nov 2022 14:23:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:590a7e1deda42fac6d1c0d281bb9ce87efb6ca3fcc7d6bcbee6bb4b7b363f378
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140913490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84065f533f3be0eb91c61d85585cba048f95b021a05244044a88027bfeaed95a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 12:29:08 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 12:49:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:49:24 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:49:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:49:29 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:49:29 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:10:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:10:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:10:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:10:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:10:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:10:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:10:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 19:10:54 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 19:15:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 19:15:21 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 19:15:21 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 19:15:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 19:15:21 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 19:15:21 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b251d39d15356abea2c79230cf242fab87ea74bcd05dd281e6f94fe97e36e4`  
		Last Modified: Sat, 12 Nov 2022 13:00:48 GMT  
		Size: 36.7 MB (36669594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a1a3e393e3b1bfc92d8653ae53a13c82581b6e927af79f7fa56cd75be265ee`  
		Last Modified: Sat, 12 Nov 2022 13:00:42 GMT  
		Size: 2.4 MB (2417705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cc7093a86ad8a89189e7286dfaaf1a732af19710a95ccc4e194c4e27fe80d8`  
		Last Modified: Sat, 12 Nov 2022 13:00:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eee7557e1106e8660cb2248f22e7a56393c67a6af0267619d9d0947e1dd68bd`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77eda6ad1a4963332eab5f01c258f2803d646f5c4b51d4831d3f396881e27e3`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 704.7 KB (704668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f04ca0a1d999700ebaa7f545e48615c0e834cc567695bca2b323052456127`  
		Last Modified: Sat, 12 Nov 2022 19:17:11 GMT  
		Size: 10.2 MB (10245678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a252b6d2d21633078745f922be7f3fbfb481def9319386ce4ac9e4fa2c54d3df`  
		Last Modified: Sat, 12 Nov 2022 19:17:34 GMT  
		Size: 88.4 MB (88445261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581a5d260656a2cf7c5a32efebbf847d7fbc8cb7a80a0db0b84aa5e6aed2ee28`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:109488734bec69a8f3a9e3a0d74b8df485083868929b5035a5098023619dc9ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135469564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34104b1dc4517c3d5722e07442f52a0368dfbd2c69d0b9ec598d7158d0552ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:56:53 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 08:11:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 08:11:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 08:11:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 08:11:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:11:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:33:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:33:51 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:33:51 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:33:51 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:34:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 11:35:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 11:35:37 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 11:35:37 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 11:35:37 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 11:35:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:35:37 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 11:35:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3f8016cbc63b3b13a298021c1681bf77749b18a9aeaf756c4d57fee9c1c72`  
		Last Modified: Sat, 12 Nov 2022 08:16:07 GMT  
		Size: 37.6 MB (37552542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789bf1647f9802940b12385260daf689771a255e5c7508874b89e3f92abd4bb`  
		Last Modified: Sat, 12 Nov 2022 08:16:03 GMT  
		Size: 2.4 MB (2425934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9f9da8b41400f1fccb3ce147e7508de0fcba2852569735aa225e7b75c98926`  
		Last Modified: Sat, 12 Nov 2022 08:16:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccbb9dc2c54dcdda274ba33cfbe3fc7919c007ab182ebe828f4a45537812cba`  
		Last Modified: Sat, 12 Nov 2022 11:36:32 GMT  
		Size: 11.1 KB (11106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609e2bb235cf901848338bf5a92bc34385f1449e2c7391d125aa348f68f121d`  
		Last Modified: Sat, 12 Nov 2022 11:36:33 GMT  
		Size: 826.3 KB (826327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b1bf97318ed9deb56c6e49a57b09ea59ad67b9bbdbba05607f8e1e348a6a2`  
		Last Modified: Sat, 12 Nov 2022 11:36:35 GMT  
		Size: 10.2 MB (10245237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd5659d555ce60351f4c2b9cdd879e16fc28499569d06240b9c2ece09f77f2`  
		Last Modified: Sat, 12 Nov 2022 11:36:45 GMT  
		Size: 81.7 MB (81699667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4d9e96b34cc176e524724e1a668b723e4ef272039b568ca961e9c423746419`  
		Last Modified: Sat, 12 Nov 2022 11:36:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.48.7`

```console
$ docker pull ghost@sha256:238d171dd5573e65d11ec1d15ce270ebf884b6029eb10387530222e3548e5814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.48.7` - linux; amd64

```console
$ docker pull ghost@sha256:68a5e602f66c84446aef747c11d0f81c35a5477c613a7bf4334ed48566e9781b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166263198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678f31e8b765746566749c4bd0cc5174d4889cb09d4f86cff04ffc47475073cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:25:19 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 13:25:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:25:42 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:25:54 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:25:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:25:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:25:55 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:32:06 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:32:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:32:17 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:32:17 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:32:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:32:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:32:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:32:45 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 23:34:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:34:17 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:34:17 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:34:17 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:34:17 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:34:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee12449a27b6cbefe837194d05282d4d28e9981b266f7f8945e0d10c5c081a0`  
		Last Modified: Tue, 15 Nov 2022 13:35:07 GMT  
		Size: 36.5 MB (36540040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90525a6fb0ebfcbd8cdb96903e3c52bccd7e7c57b7de3762924add0ba881945`  
		Last Modified: Tue, 15 Nov 2022 13:35:02 GMT  
		Size: 2.8 MB (2781637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23472a292ea8b8c6819caa310dddcc37b2b4539c444cb9983a04f6e006da09f2`  
		Last Modified: Tue, 15 Nov 2022 13:35:01 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ba2ab5cac3209b0a549ed2497636850d29fe11cd9d0cbbce5183d8f7768a8`  
		Last Modified: Tue, 15 Nov 2022 23:35:21 GMT  
		Size: 1.4 MB (1449325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596e6441777f22456d37b914015b835ec65bdf33ea364d1132c02ebd89473b3`  
		Last Modified: Tue, 15 Nov 2022 23:35:24 GMT  
		Size: 10.2 MB (10245518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0452f0dff034e8385fd87d6ff37c881007ca59792002145dc620168cfd35f34e`  
		Last Modified: Tue, 15 Nov 2022 23:35:37 GMT  
		Size: 83.8 MB (83828866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5aeb94ccb633a866500c4fc408a1f572ae6ddc9198a78c585c0376ab19f78a`  
		Last Modified: Tue, 15 Nov 2022 23:35:21 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7` - linux; arm variant v7

```console
$ docker pull ghost@sha256:de14351be64a36c8c0fed48887d7775be51f9a97d5726451c16395e3495396a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180009241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629fb91d7fdf2a0df9b71224ac9a93875de4fa89e081a46a45363f89cae0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 01:12:50 GMT
ENV NODE_VERSION=14.21.1
# Wed, 09 Nov 2022 01:13:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 01:13:13 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 01:13:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 01:13:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 01:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 01:13:26 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:51:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:51:15 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:51:15 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:51:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 09 Nov 2022 02:51:43 GMT
ENV GHOST_VERSION=4.48.7
# Wed, 09 Nov 2022 02:55:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 09 Nov 2022 02:55:55 GMT
WORKDIR /var/lib/ghost
# Wed, 09 Nov 2022 02:55:55 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 09 Nov 2022 02:55:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 09 Nov 2022 02:55:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 02:55:55 GMT
EXPOSE 2368
# Wed, 09 Nov 2022 02:55:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e93103f5a562c6a7250ddc25cfe8dff94860a97ea989f067abb9ae43d9f0c`  
		Last Modified: Wed, 09 Nov 2022 01:35:08 GMT  
		Size: 34.7 MB (34697192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91059937fcb19bb229f85b3c4bb581bc39f1b80528f4ea6bb167877811cb9181`  
		Last Modified: Wed, 09 Nov 2022 01:35:02 GMT  
		Size: 2.8 MB (2770997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9131d4652683ee7acf70dfabd07742f285353018aa436deab01cfde598d6655`  
		Last Modified: Wed, 09 Nov 2022 01:35:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904cef64f1f319bd7d8a9331083fb767b9f15761360a0f276d5d3e3d32237d12`  
		Last Modified: Wed, 09 Nov 2022 03:03:32 GMT  
		Size: 1.4 MB (1401984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71552646e26dd5c1e76eb87e66e29d408d28604b9c9ef8173585a77b1c8cb414`  
		Last Modified: Wed, 09 Nov 2022 03:03:36 GMT  
		Size: 10.2 MB (10244479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4241375b5255913ac27d83be6312c3414222e300954fa5c5e82b40fe5f4059f2`  
		Last Modified: Wed, 09 Nov 2022 03:04:01 GMT  
		Size: 104.3 MB (104310150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6d6594be7958beddfb2e49e3220814b8807288d08a3d291e19975a698459f4`  
		Last Modified: Wed, 09 Nov 2022 03:03:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:970f96f6b6e59e56760b9f0494e6a5042b22c0c0f1562c219f0699ca1a84f167
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162675660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc47c581375a83a56f6bc01b2b99ac158cef444e12fdc9adc585472e8dc3e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:47:54 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 06:48:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:48:14 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:48:24 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:48:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:48:24 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:18:58 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:19:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:19:07 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:19:07 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:19:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:19:31 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 22:20:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:20:52 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:20:52 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:20:52 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:20:52 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:20:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527a0b13fec73f848ad1b714b457491ce3ba72ddec974c5a6675bc8407fff72`  
		Last Modified: Tue, 15 Nov 2022 06:57:33 GMT  
		Size: 36.7 MB (36650706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c9297d2b26b9b0f1ec86282b9ffd0dd96345dacf0dfb9bbc45257e26ae9e4e`  
		Last Modified: Tue, 15 Nov 2022 06:57:29 GMT  
		Size: 2.8 MB (2781406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39660e2b870dc1d2f360412bc304537113d0f5d983af67635d0c7b68150a2951`  
		Last Modified: Tue, 15 Nov 2022 06:57:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7313de62eabfe7302f0a8406f13f473d8b3b9b2a427b4152691a0f8c0425ab50`  
		Last Modified: Tue, 15 Nov 2022 22:21:56 GMT  
		Size: 1.4 MB (1385216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2a95c963f5a587458f5eb1850d80cc0d1e44d5ba1dd1cb58355814b78eea7a`  
		Last Modified: Tue, 15 Nov 2022 22:21:58 GMT  
		Size: 10.2 MB (10245217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34de58bc6111651c393c9437497741489fae4eb5e450040072c21f3791497538`  
		Last Modified: Tue, 15 Nov 2022 22:22:09 GMT  
		Size: 81.5 MB (81547332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf86a8fe1dc94d1ad71b0fd6a833a8713f1392ae95845b15668136f90bf1bb5`  
		Last Modified: Tue, 15 Nov 2022 22:21:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7` - linux; ppc64le

```console
$ docker pull ghost@sha256:472108e72a9f8b7acc492222caf5f786a930445541e3fa997667e023d5e9c722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179485761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696ea1ae277858971dda69656400ecd1354bba2cb4af681fe5133a568eada427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:10:01 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 18:10:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:10:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:11:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:11:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:11:11 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:27:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:27:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:27:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:27:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:28:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:28:39 GMT
ENV GHOST_VERSION=4.48.7
# Tue, 15 Nov 2022 19:36:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:37:06 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:37:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:37:07 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:37:09 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:37:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280fd52e4db435fcfbd4455998ab6b003a18dd9c81667a19e4932662d1b6d23`  
		Last Modified: Tue, 15 Nov 2022 18:21:04 GMT  
		Size: 38.5 MB (38465872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2810c606a78bf1e5de3f9bd19ebc774867cdfb5cd664b77fa05f40a988a5d8be`  
		Last Modified: Tue, 15 Nov 2022 18:20:55 GMT  
		Size: 2.8 MB (2781533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c7cb0647ab1994480257ba0718c71cec8235dbb7b6c6ea3b13ec601efabfc`  
		Last Modified: Tue, 15 Nov 2022 18:20:54 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb544f8f9262f08664b3cb6a8dbadf395832983093416f34742c0237532b76d`  
		Last Modified: Tue, 15 Nov 2022 19:38:47 GMT  
		Size: 1.4 MB (1369041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa1da6b1ecc386866a81422b350eb365fff97858ad90a64e0cf950d4826dad`  
		Last Modified: Tue, 15 Nov 2022 19:38:52 GMT  
		Size: 10.2 MB (10245733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d05097413d17963f366e8b00a52c591d70ea06dd70c892a31afd3e8e0c16a17`  
		Last Modified: Tue, 15 Nov 2022 19:39:21 GMT  
		Size: 91.3 MB (91333264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcff9c647fc44136b0a623cae47edf0cadcbeff19e8e9f89557918c550023b2`  
		Last Modified: Tue, 15 Nov 2022 19:38:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7` - linux; s390x

```console
$ docker pull ghost@sha256:39c0136ef28c1012eca95f7941f55c36e768fea34de2c6b22321a960a471e90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171267829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66794ea866fbed5d851c0a50533ec3bd396d890166b98dbfc348dd316ab76351`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:13:33 GMT
ENV NODE_VERSION=14.21.1
# Tue, 15 Nov 2022 08:14:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:14:27 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:14:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:14:57 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:14:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:14:58 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:21:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:21:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:21:44 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:21:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:22:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:22:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:22:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:22:48 GMT
ENV GHOST_VERSION=4.48.7
# Wed, 16 Nov 2022 01:35:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:35:52 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:35:53 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:35:53 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:35:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:35:54 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:35:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669536de4c4a877c9ba64dea9a85cb2082decdef35f73674dae78c727a09b286`  
		Last Modified: Tue, 15 Nov 2022 08:23:06 GMT  
		Size: 36.4 MB (36407040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7640ec25984afbdb2a21ba06f2bad09dd9d32018133b8fed325615f9709005e`  
		Last Modified: Tue, 15 Nov 2022 08:23:02 GMT  
		Size: 2.8 MB (2784207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5265e89340cb1ee22fa6df2f166f26abeb1d324bd1c9b50867d01557ac5fab28`  
		Last Modified: Tue, 15 Nov 2022 08:23:01 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ff8a26c0e98944b7aa11f47161560bda78ab1a2e0d348b6a4796de17da7aac`  
		Last Modified: Wed, 16 Nov 2022 01:36:55 GMT  
		Size: 1.4 MB (1436325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204491b21c117e8e97183d92778f5ceb48cb63f57e6c0202c99b544d6ff22c2`  
		Last Modified: Wed, 16 Nov 2022 01:36:57 GMT  
		Size: 10.2 MB (10245601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ce9194dd83160c5de6b20bac633cb8d0a4e43fe4f7856fe9c87cada7b5ce0`  
		Last Modified: Wed, 16 Nov 2022 01:37:11 GMT  
		Size: 90.7 MB (90745687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c706a7bd2e6cf3713b984afce47b02b2a20d0a8785d5cca3963056fe200a0188`  
		Last Modified: Wed, 16 Nov 2022 01:36:54 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.48.7-alpine`

```console
$ docker pull ghost@sha256:3cb4e563b6c8f96fd5f19aeae32a19892bf34e71c56f83f45953f7479d69f766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4.48.7-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4da829f81b6fed3d63296fb4d33e5593a2ecb9e3fcfc8a45c18ffff44c82a5c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138529046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f590d33bc1954519265b3e6845d64c446521ba4988e742b01f58cca69086747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:32:07 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 06:32:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:32:16 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:32:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:32:20 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:32:20 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:27:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:27:36 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:27:36 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:27:36 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 11:28:01 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 11:29:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 11:29:39 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 11:29:39 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 11:29:40 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 11:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:29:40 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 11:29:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c774934c91f00c542a1fb93212d42cf819d47de47169f00eba8db7e7026f51`  
		Last Modified: Sat, 12 Nov 2022 06:37:20 GMT  
		Size: 37.7 MB (37724346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d9211bf297cc0df2b07d2ad8ee5a83f5f479165228a1a513004dba925cfc20`  
		Last Modified: Sat, 12 Nov 2022 06:37:15 GMT  
		Size: 2.4 MB (2368725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14523e6c1be223f204f3266fd2d66cc5d9caf28f41364bfa565923c09ed3b4db`  
		Last Modified: Sat, 12 Nov 2022 06:37:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6df5a33c8d055ce1259d2b29b7854405e699e1b444b523db9b1bf8342f9fc26`  
		Last Modified: Sat, 12 Nov 2022 11:30:32 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cf5c4a5c5408e30aa38cc30b22c9d22699130f32b2537db3e4ef7316ad003`  
		Last Modified: Sat, 12 Nov 2022 11:30:32 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5fa079d29a8020c2f30554dec49ebf6b4f476258dfcd337a6dd3d7e982384`  
		Last Modified: Sat, 12 Nov 2022 11:30:35 GMT  
		Size: 10.2 MB (10245542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3922449be4564a3926b8b3bf9782d9773df8f0472787745a4e72f69111cd2dc5`  
		Last Modified: Sat, 12 Nov 2022 11:30:48 GMT  
		Size: 84.6 MB (84551804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7770868a814ace688266d135c566d8caa4e4e0380a8f185e670df92dd721e21c`  
		Last Modified: Sat, 12 Nov 2022 11:30:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:610087d2d38d72249bb2282bb5a7aa1c3f5d67a1c7b434a076b6869de6e89190
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142193449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced480230185dbe29a7675ff123e589acc9f220b5be61090060f623eb7ece52f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 10:49:14 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 11:23:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 11:23:48 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 11:23:54 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 11:23:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 11:23:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:23:55 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:15:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:15:58 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:15:58 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:15:58 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:16:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 14:16:36 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 14:22:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 14:22:23 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 14:22:23 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 14:22:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 14:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 14:22:23 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 14:22:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2013ca6af2177095883e23da431551e40beacbe9b328bd9a64b101c7afb7af44`  
		Last Modified: Sat, 12 Nov 2022 11:29:32 GMT  
		Size: 36.7 MB (36749486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206761edc1c09db4001f2e6e0ec7451ce3e09df10209b08330620e64ac1a5ba4`  
		Last Modified: Sat, 12 Nov 2022 11:29:25 GMT  
		Size: 2.4 MB (2417570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b20dd6b1b095cad4cf131f991c687c89721cc3b787ad3f134c76b75472b8d9`  
		Last Modified: Sat, 12 Nov 2022 11:29:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0af623f089836b4d1c0948bdf9f60e6d9b0cb1cb213e3b91310aabc839fd16`  
		Last Modified: Sat, 12 Nov 2022 14:23:48 GMT  
		Size: 11.0 KB (10992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f949fa7d5d18587a9c4c5bd0ecf584329557957f7f2c2ef1a8c2a292e8112a72`  
		Last Modified: Sat, 12 Nov 2022 14:23:49 GMT  
		Size: 772.0 KB (771958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddc36407495dd1762664fbc5aa936ce3a4ab1dd65adebc12a2a166c5e01a64`  
		Last Modified: Sat, 12 Nov 2022 14:23:53 GMT  
		Size: 10.2 MB (10245693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d200752754072d904b9125051ec21f3ea13656be04575118afbe4763ccf301`  
		Last Modified: Sat, 12 Nov 2022 14:24:16 GMT  
		Size: 89.4 MB (89381646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910bc20053c92e69bbb19f3c7fd368ded5cf3982e1f234fe2fca6ec74ae0f8e`  
		Last Modified: Sat, 12 Nov 2022 14:23:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:590a7e1deda42fac6d1c0d281bb9ce87efb6ca3fcc7d6bcbee6bb4b7b363f378
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140913490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84065f533f3be0eb91c61d85585cba048f95b021a05244044a88027bfeaed95a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 12:29:08 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 12:49:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:49:24 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:49:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:49:29 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:49:29 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:10:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:10:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:10:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:10:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:10:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:10:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:10:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 19:10:54 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 19:15:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 19:15:21 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 19:15:21 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 19:15:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 19:15:21 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 19:15:21 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b251d39d15356abea2c79230cf242fab87ea74bcd05dd281e6f94fe97e36e4`  
		Last Modified: Sat, 12 Nov 2022 13:00:48 GMT  
		Size: 36.7 MB (36669594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a1a3e393e3b1bfc92d8653ae53a13c82581b6e927af79f7fa56cd75be265ee`  
		Last Modified: Sat, 12 Nov 2022 13:00:42 GMT  
		Size: 2.4 MB (2417705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cc7093a86ad8a89189e7286dfaaf1a732af19710a95ccc4e194c4e27fe80d8`  
		Last Modified: Sat, 12 Nov 2022 13:00:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eee7557e1106e8660cb2248f22e7a56393c67a6af0267619d9d0947e1dd68bd`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77eda6ad1a4963332eab5f01c258f2803d646f5c4b51d4831d3f396881e27e3`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 704.7 KB (704668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f04ca0a1d999700ebaa7f545e48615c0e834cc567695bca2b323052456127`  
		Last Modified: Sat, 12 Nov 2022 19:17:11 GMT  
		Size: 10.2 MB (10245678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a252b6d2d21633078745f922be7f3fbfb481def9319386ce4ac9e4fa2c54d3df`  
		Last Modified: Sat, 12 Nov 2022 19:17:34 GMT  
		Size: 88.4 MB (88445261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581a5d260656a2cf7c5a32efebbf847d7fbc8cb7a80a0db0b84aa5e6aed2ee28`  
		Last Modified: Sat, 12 Nov 2022 19:17:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.48.7-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:109488734bec69a8f3a9e3a0d74b8df485083868929b5035a5098023619dc9ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135469564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34104b1dc4517c3d5722e07442f52a0368dfbd2c69d0b9ec598d7158d0552ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:56:53 GMT
ENV NODE_VERSION=14.21.1
# Sat, 12 Nov 2022 08:11:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0fc7c18a1fa7aa6b39ac7b11ba2e56fa12ab1c4d3b4bb32f9c4ac3f7178d613c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 08:11:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 08:11:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 08:11:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:11:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:33:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:33:51 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:33:51 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:33:51 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:34:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 12 Nov 2022 11:34:12 GMT
ENV GHOST_VERSION=4.48.7
# Sat, 12 Nov 2022 11:35:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 12 Nov 2022 11:35:37 GMT
WORKDIR /var/lib/ghost
# Sat, 12 Nov 2022 11:35:37 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 12 Nov 2022 11:35:37 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 12 Nov 2022 11:35:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 11:35:37 GMT
EXPOSE 2368
# Sat, 12 Nov 2022 11:35:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3f8016cbc63b3b13a298021c1681bf77749b18a9aeaf756c4d57fee9c1c72`  
		Last Modified: Sat, 12 Nov 2022 08:16:07 GMT  
		Size: 37.6 MB (37552542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789bf1647f9802940b12385260daf689771a255e5c7508874b89e3f92abd4bb`  
		Last Modified: Sat, 12 Nov 2022 08:16:03 GMT  
		Size: 2.4 MB (2425934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9f9da8b41400f1fccb3ce147e7508de0fcba2852569735aa225e7b75c98926`  
		Last Modified: Sat, 12 Nov 2022 08:16:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccbb9dc2c54dcdda274ba33cfbe3fc7919c007ab182ebe828f4a45537812cba`  
		Last Modified: Sat, 12 Nov 2022 11:36:32 GMT  
		Size: 11.1 KB (11106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609e2bb235cf901848338bf5a92bc34385f1449e2c7391d125aa348f68f121d`  
		Last Modified: Sat, 12 Nov 2022 11:36:33 GMT  
		Size: 826.3 KB (826327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b1bf97318ed9deb56c6e49a57b09ea59ad67b9bbdbba05607f8e1e348a6a2`  
		Last Modified: Sat, 12 Nov 2022 11:36:35 GMT  
		Size: 10.2 MB (10245237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd5659d555ce60351f4c2b9cdd879e16fc28499569d06240b9c2ece09f77f2`  
		Last Modified: Sat, 12 Nov 2022 11:36:45 GMT  
		Size: 81.7 MB (81699667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4d9e96b34cc176e524724e1a668b723e4ef272039b568ca961e9c423746419`  
		Last Modified: Sat, 12 Nov 2022 11:36:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5`

```console
$ docker pull ghost@sha256:8b755f1acec31e63c8575a57fba0ff5cb5201ea858a4e9c2ad275bed9002b293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:5` - linux; amd64

```console
$ docker pull ghost@sha256:d7dc14254fd5b6bcc96d8a45fa5ab054301fdc2c62a8570a2da0fc0c7163f7bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161548556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001188daca9de3e0d946e910a97f19f2931348014b0450df3b099ed453c1ca78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:23:13 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 13:23:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:23:36 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:23:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:23:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:23:48 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:29:40 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:29:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:29:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:29:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:30:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 23:31:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:31:54 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:31:54 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:31:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:31:55 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:31:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf4d46bb2489b83c7602534e5a2651218fd890a70cb89e67f6905c82e41519`  
		Last Modified: Tue, 15 Nov 2022 13:33:34 GMT  
		Size: 35.5 MB (35459473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e3331ed6131ec5f8247e6c10a2cf1bfe5decf0ea27caf108da39bf2acc8640`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 2.8 MB (2764146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec19194f61cd61071c240ceb80b7bc7253268a781e4b1867ebbd561c38d6c5`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72c90f807760e639efc513b89a178ebc89b9f997b3b1d9377504c4f73fcdf75`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 1.4 MB (1449283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea25c46896f120f002dd87c9998cebabbbbdb49a181c8257baac42ed90a2fc`  
		Last Modified: Tue, 15 Nov 2022 23:34:49 GMT  
		Size: 10.2 MB (10221363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdb760963cb9640c173e3d3cf19be1fffa7c6b74bb933e287e0a06c0950a2a5`  
		Last Modified: Tue, 15 Nov 2022 23:35:03 GMT  
		Size: 80.2 MB (80236481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f277ce8b6640231de36cd96b2dd3774fc89c3ec080711c2c1b51eb918fd1a4`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1287661a59dd3f5ab9f7b32d3d6fafefd27c9516c823ecd6a75d70814cda3591
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165783911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e481eae5257a93529264d3c19f279dc7de887154272f5e02bbd226183a30fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 00:14:01 GMT
ENV NODE_VERSION=16.18.1
# Wed, 09 Nov 2022 00:14:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 00:14:25 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 00:14:39 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 00:14:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 00:14:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 00:14:39 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:36:34 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:36:47 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:36:47 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:37:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:39:59 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:45:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:45:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:45:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:45:21 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 00:45:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:45:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:45:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea8153e91aead518fb126da6eaa6a5537bab1e59ccf5158259758e7eb52023`  
		Last Modified: Wed, 09 Nov 2022 01:31:43 GMT  
		Size: 32.7 MB (32674064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347d8b382bcc282f50e1852663f7bb13e02fcb73c5aefd2941d560301c77513`  
		Last Modified: Wed, 09 Nov 2022 01:31:37 GMT  
		Size: 2.8 MB (2754357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad09949a32d06a6c9bcdda5c737a82fe18c5150f06ce1f8d3748775844f6ebcc`  
		Last Modified: Wed, 09 Nov 2022 01:31:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd827919251e7f3fd55d8971a48ac80d30260a48bb44aaabc96aa3107a0be126`  
		Last Modified: Wed, 09 Nov 2022 03:01:55 GMT  
		Size: 1.4 MB (1401933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b582ead2fdbe8a32cf94e60cbb709733a8fe6cfcef9c123a01146c628de9f0`  
		Last Modified: Wed, 09 Nov 2022 03:01:59 GMT  
		Size: 10.2 MB (10222051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e794c1499dcd232c94c502ae0fdf10cd0bfb996c1b8606365ee1efe5de6a56`  
		Last Modified: Tue, 15 Nov 2022 00:55:01 GMT  
		Size: 92.1 MB (92147067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d89048947e4277b5c42b31a44a2e499e87d964ae6d6984644c2b480a6c64b3`  
		Last Modified: Tue, 15 Nov 2022 00:54:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d353e6327748fe7f3363f0d61fd592cddd8b358cb13b2f276c837b78a7f1b142
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169075352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8643932b495135341e6d425cb9a2a5542064fb78a4ee04c98845e04e663801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:45:59 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 06:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:46:18 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:46:27 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:46:27 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:46:28 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:14:33 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:14:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:14:44 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:14:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:14:57 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 22:18:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:18:47 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:18:47 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:18:47 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:18:48 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:18:48 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6818cad41f1d340b619ad94fcdeba483b7d959319c2b05023bc3b3d032dd9fe`  
		Last Modified: Tue, 15 Nov 2022 06:55:57 GMT  
		Size: 35.7 MB (35700928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec1e2eaae6f47edd60f65027854a48a59d04160e1f602f9612f282bed16bfb`  
		Last Modified: Tue, 15 Nov 2022 06:55:54 GMT  
		Size: 2.8 MB (2763892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8318b016de3ae2c2e9ea562bcdef9e07680e94e75a09ccb997bba3a940c82`  
		Last Modified: Tue, 15 Nov 2022 06:55:53 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37965a6a28429507a0443198d6fb57eb92bf02b4825ffe3050533544267ed328`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 1.4 MB (1385222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d2cdfd6571f64df92ce24977dcfda34fd83f1badfd1b7e3a0d84746d9f967`  
		Last Modified: Tue, 15 Nov 2022 22:21:28 GMT  
		Size: 10.2 MB (10220713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1ed3bef567b2ff43af194597b8f0387ad3d62ac40c1476ede48fecb4c30ac`  
		Last Modified: Tue, 15 Nov 2022 22:21:41 GMT  
		Size: 88.9 MB (88938811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a980f49926890e46de7153fd1e518c6970381fb09e6cec2c10d7e4ece030e96`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:cfa5bacef385f8968406e20d27059d8e073ecddf5f5a6e32a2810ef7845924ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165351765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d32af16b262d202f6e92061a74f8e48459bfb471f6399c09512bfbc700342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:07:48 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 18:08:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:08:29 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:08:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:08:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:08:57 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:16:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:16:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:16:24 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:16:24 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:16:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 19:27:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:27:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:27:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:27:22 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:27:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:27:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc704eecace49db0b3b527128a9c246649c5b01952bc85cd0cb619ba871036`  
		Last Modified: Tue, 15 Nov 2022 18:19:51 GMT  
		Size: 37.5 MB (37514111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3448e957aebe054316bec55eeb7221f6c31178f34d53401774228b5168e7c0b`  
		Last Modified: Tue, 15 Nov 2022 18:19:42 GMT  
		Size: 2.8 MB (2764077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e5af461d4b8e4bc212e2164deb20339ce80e9777e0702fb326ad1df21c5e8f`  
		Last Modified: Tue, 15 Nov 2022 18:19:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96460bc859bb7bc52cc87115370348e9cbb870e4a9f31db19ebfca0ee700330`  
		Last Modified: Tue, 15 Nov 2022 19:37:47 GMT  
		Size: 1.4 MB (1369026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a06b8efc7b2887731416d83a3d4bf5dac060651aa86ec09c724aacef8a1a56`  
		Last Modified: Tue, 15 Nov 2022 19:37:52 GMT  
		Size: 10.2 MB (10227513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cc7197a5eeb2c64335942f83bacd788eceab7a3fe59bbf1de22ec37020e313`  
		Last Modified: Tue, 15 Nov 2022 19:38:18 GMT  
		Size: 78.2 MB (78186722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcb4f5472c1392866505e519ff2726624578a41dd12dc955876f2f479ecd04`  
		Last Modified: Tue, 15 Nov 2022 19:37:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:e49397a5850f441fb801a76b0a5c81a4ba36a003a26d920af55a42847da1dac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157552613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18d55cd8f8f97f9411189baf6f322687c8c6f01e998a0069796bade80e917e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:11:20 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 08:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:12:01 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:12:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:12:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:12:23 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:11:05 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:11:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:11:30 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:11:31 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:12:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:12:12 GMT
ENV GHOST_VERSION=5.22.10
# Wed, 16 Nov 2022 01:20:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:21:15 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:21:15 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:21:16 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:21:17 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:21:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fda3a1e3ada00d249bc778488a797425cf7cd8050e77843ebeb0f5ea62f224`  
		Last Modified: Tue, 15 Nov 2022 08:22:25 GMT  
		Size: 35.4 MB (35370246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d9e5094e9573f77781bb698c378fad5e70b19e7980e000ecbfe5bbf2e5a500`  
		Last Modified: Tue, 15 Nov 2022 08:22:20 GMT  
		Size: 2.8 MB (2765674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553feeb25b7cd32c8934573fc885496b40e5ff89cf4bef4aae6d587b6d10cb2`  
		Last Modified: Tue, 15 Nov 2022 08:22:19 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8623d720f3c42dbe1854a0f481b08794fc213ed352d16b8208c1e0bc75e8fb`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 1.4 MB (1436312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c0510e8a3cd0f1b7a3ce052b46d206d04bad03bce28a3d60ed79d02f2b0c57`  
		Last Modified: Wed, 16 Nov 2022 01:36:29 GMT  
		Size: 10.2 MB (10225396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596217afd671d877e64627a6697d89fcd62931b8ecad3beccd820614a3d2cf5`  
		Last Modified: Wed, 16 Nov 2022 01:36:42 GMT  
		Size: 78.1 MB (78106018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabdd107e4fb17c5e0b38ff8aee93fa48afa5019343da9a5f945332195fa946`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:dcda6872d81dad08a1fa9c45d11b0836759fca6de897ee2ecd8f06e9c774d28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:839e74e0be715e1164e0286d25623233b65bec72f5c49d1653fddbc789609d74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133735107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba65fa4741d3de85fecf5dfb61d1e46809bd209088bec4cda4927748243dbb0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:31:38 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 06:31:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:31:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:31:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:31:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:31:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:31:51 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:25:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:25:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:25:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:25:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:25:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:23:52 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:25:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:25:41 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:25:41 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:25:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:25:41 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:25:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb1b25da51088e0fd1776f0b761b6d6b10d19b644e4c0d2a0e7c6d2237d8c65`  
		Last Modified: Sat, 12 Nov 2022 06:36:36 GMT  
		Size: 36.6 MB (36574826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604515c95e115c675e3e4467f77080c2aee4759272fa78161bde7a9536ef169`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 2.4 MB (2351149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bf7dff8d854e790d3475c79af59120a2f578bf057c5ed4512d19839649c41f`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d9e36250dcfd97ebc121e69a9856496b40b92ae7aa858eeff8806b81e4e9a`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 11.3 KB (11293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3f18cf69e59f39475d0dace45f0aca55c6b78bc13441a07b261bd928c76f0`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38893683f95f259b97b62421595bee0c4cdf2cbe2f4ffd4798777de70f4893d6`  
		Last Modified: Sat, 12 Nov 2022 11:30:02 GMT  
		Size: 10.2 MB (10221109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5db84843950d5baac2d64b7b859550e2611399ca90b5b81746cbe90fbe4db7`  
		Last Modified: Tue, 15 Nov 2022 01:26:50 GMT  
		Size: 80.9 MB (80949393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12c7ed583754de5cd2bfb1bcb57c3284cb0ab6c6b753e189ab7db63d9b4cb42`  
		Last Modified: Tue, 15 Nov 2022 01:26:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:0ae556437c35ee790aab65cfe9f7417201e0356da7682abcd3fcbfd92965a3d1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730cc2688da47e562d5330cadb00d4190e2cbcba37c78d2abfe3baebf4aaf6b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:59:51 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 10:48:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 10:48:42 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 10:48:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 10:48:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 10:48:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 10:48:49 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:04:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:04:43 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:04:43 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:04:43 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:05:18 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:49:26 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:59:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 02:00:03 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 02:00:04 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 02:00:04 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 02:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 02:00:04 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 02:00:04 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f611d26fd649b9911106001558a1fc88106d042a4a58f18d143f315bb9b4d`  
		Last Modified: Sat, 12 Nov 2022 11:28:47 GMT  
		Size: 35.5 MB (35511547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375aad15b0390a11efe0d2624016142a73d3d40b4d08f5f7bd4ae5a2a0ce8f4b`  
		Last Modified: Sat, 12 Nov 2022 11:28:40 GMT  
		Size: 2.4 MB (2399842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e182de8dbbe31b087dae17062287b2276c9f9505251aeeef2e23f31241cc6`  
		Last Modified: Sat, 12 Nov 2022 11:28:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8bc1a231aa404a6ade4980ed81c0ea8d471ca420441c9b9975e8771d9b9734`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a546cf8571bd364a88c8604b1f78d1ccb7e6ea476b9e6eb0a38bc2cc56771536`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 772.0 KB (771952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b890066ace05ae48e45e47baa1072b801c4eedc7c84c99cc2c977c1ecb300`  
		Last Modified: Sat, 12 Nov 2022 14:23:07 GMT  
		Size: 10.2 MB (10227843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade4e0a4ec2f548f3f3ae429a94f370b249e93a2c12eafa0f0b9b429d4090c33`  
		Last Modified: Tue, 15 Nov 2022 02:01:06 GMT  
		Size: 76.6 MB (76618482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d6a5c7c0cfee38eb3f1196a722a5e912b687d8fd92143ad67b740b02750e0e`  
		Last Modified: Tue, 15 Nov 2022 02:00:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:9ce397fd004a94e2d921db724d8a3b5a9583f547c275efd5c6ce292da89ee408
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127104574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f09e32a5d7431988116ac7a5fe5a6f42dca52b43d8b7cf8635497f40019d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 11:57:52 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 12:28:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:28:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:28:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:28:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:28:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:01:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:01:50 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:01:50 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:01:50 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:02:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:45:29 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:53:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:53:32 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:53:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:53:32 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 00:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:53:32 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:53:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7581c8bbcf3ca02b56e1a9918948b1ecc5cc42131183451ab49aa66298a1ec`  
		Last Modified: Sat, 12 Nov 2022 12:59:40 GMT  
		Size: 35.4 MB (35404696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35120aff68c6f2f54066d564e25aa456a7d9452efd293597199f383882d637a4`  
		Last Modified: Sat, 12 Nov 2022 12:59:34 GMT  
		Size: 2.4 MB (2399918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14500faf614ce3be69f3bc4ba6664fe44fbbeec08e7b61bfd42ce6fb2438aad6`  
		Last Modified: Sat, 12 Nov 2022 12:59:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98613b1b56088e4eef1b04242d4e188e2f8b077a5ea65adf0cf5ffb6b01a3a50`  
		Last Modified: Sat, 12 Nov 2022 19:16:18 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe4ed4bafa4dcfb63b31ccc68142925eaf4be440b10fc109739768021c1f49`  
		Last Modified: Sat, 12 Nov 2022 19:16:19 GMT  
		Size: 704.7 KB (704659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5a19c40ad574aba78b769bb4ab0e8cbf695607710abb22f2b58d83087e2425`  
		Last Modified: Sat, 12 Nov 2022 19:16:23 GMT  
		Size: 10.2 MB (10223784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88b7f8a0c682fc0fb671afeaf1e7ee84f0e4e7bbbe47ebb55a15b023be2fdf`  
		Last Modified: Tue, 15 Nov 2022 00:55:45 GMT  
		Size: 75.9 MB (75940925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a41741ce8e0495a1e872512ccb3d52f4a24677d4102ab0ddcec7c160e53e0`  
		Last Modified: Tue, 15 Nov 2022 00:55:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:00b7db4c7a9bf160965498a023ad445f3bd59008c44644ae40e3685b2f495b64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141137165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5520e3ef968d5d21f55d7e04e19dc45be48e6c3a21f7d305672d39be722957c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:35:18 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 07:56:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 07:56:29 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 07:56:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 07:56:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:56:34 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:28:42 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:28:42 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:52:10 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:56:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:56:44 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:56:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:56:44 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:56:45 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:56:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28d7a0466a25c2824be774476f9c384891186b778c555fcd8cb70af320542ed`  
		Last Modified: Sat, 12 Nov 2022 08:15:29 GMT  
		Size: 36.4 MB (36428230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9597b1f237244220e9b5a52e75a0dc0f83031769f7549714f054f9af171e9e8`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 2.4 MB (2409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b006997bfe605f7d900583d90ddb61607a413baab97cea3d9b1154bfffc647`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96d881df569f57ca62d15673dcda76415a92994a1f1529aa3ec29945b9fc3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 11.1 KB (11097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da976d62d65f9b3862540036123d404465e8c65071532e9c00aa448b828c9f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 826.3 KB (826332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22c77cb9064d92dde89b1d391cd64160dac54c1885014df2384a35ac3a2ea3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:03 GMT  
		Size: 10.2 MB (10220636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd9457bd3eeb7afe3a047c7f0020c445979cd618eddde7482db65d1d5668513`  
		Last Modified: Tue, 15 Nov 2022 01:57:51 GMT  
		Size: 88.5 MB (88532795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3fd9b068511adc832a6bb38c60f4c321942c249bb31bfd179b199855820b42`  
		Last Modified: Tue, 15 Nov 2022 01:57:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.22`

```console
$ docker pull ghost@sha256:8b755f1acec31e63c8575a57fba0ff5cb5201ea858a4e9c2ad275bed9002b293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:5.22` - linux; amd64

```console
$ docker pull ghost@sha256:d7dc14254fd5b6bcc96d8a45fa5ab054301fdc2c62a8570a2da0fc0c7163f7bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161548556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001188daca9de3e0d946e910a97f19f2931348014b0450df3b099ed453c1ca78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:23:13 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 13:23:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:23:36 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:23:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:23:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:23:48 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:29:40 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:29:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:29:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:29:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:30:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 23:31:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:31:54 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:31:54 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:31:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:31:55 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:31:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf4d46bb2489b83c7602534e5a2651218fd890a70cb89e67f6905c82e41519`  
		Last Modified: Tue, 15 Nov 2022 13:33:34 GMT  
		Size: 35.5 MB (35459473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e3331ed6131ec5f8247e6c10a2cf1bfe5decf0ea27caf108da39bf2acc8640`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 2.8 MB (2764146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec19194f61cd61071c240ceb80b7bc7253268a781e4b1867ebbd561c38d6c5`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72c90f807760e639efc513b89a178ebc89b9f997b3b1d9377504c4f73fcdf75`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 1.4 MB (1449283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea25c46896f120f002dd87c9998cebabbbbdb49a181c8257baac42ed90a2fc`  
		Last Modified: Tue, 15 Nov 2022 23:34:49 GMT  
		Size: 10.2 MB (10221363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdb760963cb9640c173e3d3cf19be1fffa7c6b74bb933e287e0a06c0950a2a5`  
		Last Modified: Tue, 15 Nov 2022 23:35:03 GMT  
		Size: 80.2 MB (80236481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f277ce8b6640231de36cd96b2dd3774fc89c3ec080711c2c1b51eb918fd1a4`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1287661a59dd3f5ab9f7b32d3d6fafefd27c9516c823ecd6a75d70814cda3591
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165783911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e481eae5257a93529264d3c19f279dc7de887154272f5e02bbd226183a30fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 00:14:01 GMT
ENV NODE_VERSION=16.18.1
# Wed, 09 Nov 2022 00:14:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 00:14:25 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 00:14:39 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 00:14:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 00:14:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 00:14:39 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:36:34 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:36:47 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:36:47 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:37:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:39:59 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:45:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:45:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:45:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:45:21 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 00:45:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:45:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:45:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea8153e91aead518fb126da6eaa6a5537bab1e59ccf5158259758e7eb52023`  
		Last Modified: Wed, 09 Nov 2022 01:31:43 GMT  
		Size: 32.7 MB (32674064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347d8b382bcc282f50e1852663f7bb13e02fcb73c5aefd2941d560301c77513`  
		Last Modified: Wed, 09 Nov 2022 01:31:37 GMT  
		Size: 2.8 MB (2754357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad09949a32d06a6c9bcdda5c737a82fe18c5150f06ce1f8d3748775844f6ebcc`  
		Last Modified: Wed, 09 Nov 2022 01:31:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd827919251e7f3fd55d8971a48ac80d30260a48bb44aaabc96aa3107a0be126`  
		Last Modified: Wed, 09 Nov 2022 03:01:55 GMT  
		Size: 1.4 MB (1401933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b582ead2fdbe8a32cf94e60cbb709733a8fe6cfcef9c123a01146c628de9f0`  
		Last Modified: Wed, 09 Nov 2022 03:01:59 GMT  
		Size: 10.2 MB (10222051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e794c1499dcd232c94c502ae0fdf10cd0bfb996c1b8606365ee1efe5de6a56`  
		Last Modified: Tue, 15 Nov 2022 00:55:01 GMT  
		Size: 92.1 MB (92147067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d89048947e4277b5c42b31a44a2e499e87d964ae6d6984644c2b480a6c64b3`  
		Last Modified: Tue, 15 Nov 2022 00:54:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d353e6327748fe7f3363f0d61fd592cddd8b358cb13b2f276c837b78a7f1b142
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169075352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8643932b495135341e6d425cb9a2a5542064fb78a4ee04c98845e04e663801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:45:59 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 06:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:46:18 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:46:27 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:46:27 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:46:28 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:14:33 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:14:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:14:44 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:14:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:14:57 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 22:18:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:18:47 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:18:47 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:18:47 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:18:48 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:18:48 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6818cad41f1d340b619ad94fcdeba483b7d959319c2b05023bc3b3d032dd9fe`  
		Last Modified: Tue, 15 Nov 2022 06:55:57 GMT  
		Size: 35.7 MB (35700928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec1e2eaae6f47edd60f65027854a48a59d04160e1f602f9612f282bed16bfb`  
		Last Modified: Tue, 15 Nov 2022 06:55:54 GMT  
		Size: 2.8 MB (2763892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8318b016de3ae2c2e9ea562bcdef9e07680e94e75a09ccb997bba3a940c82`  
		Last Modified: Tue, 15 Nov 2022 06:55:53 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37965a6a28429507a0443198d6fb57eb92bf02b4825ffe3050533544267ed328`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 1.4 MB (1385222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d2cdfd6571f64df92ce24977dcfda34fd83f1badfd1b7e3a0d84746d9f967`  
		Last Modified: Tue, 15 Nov 2022 22:21:28 GMT  
		Size: 10.2 MB (10220713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1ed3bef567b2ff43af194597b8f0387ad3d62ac40c1476ede48fecb4c30ac`  
		Last Modified: Tue, 15 Nov 2022 22:21:41 GMT  
		Size: 88.9 MB (88938811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a980f49926890e46de7153fd1e518c6970381fb09e6cec2c10d7e4ece030e96`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22` - linux; ppc64le

```console
$ docker pull ghost@sha256:cfa5bacef385f8968406e20d27059d8e073ecddf5f5a6e32a2810ef7845924ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165351765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d32af16b262d202f6e92061a74f8e48459bfb471f6399c09512bfbc700342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:07:48 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 18:08:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:08:29 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:08:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:08:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:08:57 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:16:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:16:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:16:24 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:16:24 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:16:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 19:27:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:27:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:27:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:27:22 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:27:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:27:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc704eecace49db0b3b527128a9c246649c5b01952bc85cd0cb619ba871036`  
		Last Modified: Tue, 15 Nov 2022 18:19:51 GMT  
		Size: 37.5 MB (37514111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3448e957aebe054316bec55eeb7221f6c31178f34d53401774228b5168e7c0b`  
		Last Modified: Tue, 15 Nov 2022 18:19:42 GMT  
		Size: 2.8 MB (2764077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e5af461d4b8e4bc212e2164deb20339ce80e9777e0702fb326ad1df21c5e8f`  
		Last Modified: Tue, 15 Nov 2022 18:19:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96460bc859bb7bc52cc87115370348e9cbb870e4a9f31db19ebfca0ee700330`  
		Last Modified: Tue, 15 Nov 2022 19:37:47 GMT  
		Size: 1.4 MB (1369026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a06b8efc7b2887731416d83a3d4bf5dac060651aa86ec09c724aacef8a1a56`  
		Last Modified: Tue, 15 Nov 2022 19:37:52 GMT  
		Size: 10.2 MB (10227513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cc7197a5eeb2c64335942f83bacd788eceab7a3fe59bbf1de22ec37020e313`  
		Last Modified: Tue, 15 Nov 2022 19:38:18 GMT  
		Size: 78.2 MB (78186722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcb4f5472c1392866505e519ff2726624578a41dd12dc955876f2f479ecd04`  
		Last Modified: Tue, 15 Nov 2022 19:37:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22` - linux; s390x

```console
$ docker pull ghost@sha256:e49397a5850f441fb801a76b0a5c81a4ba36a003a26d920af55a42847da1dac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157552613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18d55cd8f8f97f9411189baf6f322687c8c6f01e998a0069796bade80e917e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:11:20 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 08:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:12:01 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:12:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:12:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:12:23 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:11:05 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:11:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:11:30 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:11:31 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:12:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:12:12 GMT
ENV GHOST_VERSION=5.22.10
# Wed, 16 Nov 2022 01:20:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:21:15 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:21:15 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:21:16 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:21:17 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:21:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fda3a1e3ada00d249bc778488a797425cf7cd8050e77843ebeb0f5ea62f224`  
		Last Modified: Tue, 15 Nov 2022 08:22:25 GMT  
		Size: 35.4 MB (35370246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d9e5094e9573f77781bb698c378fad5e70b19e7980e000ecbfe5bbf2e5a500`  
		Last Modified: Tue, 15 Nov 2022 08:22:20 GMT  
		Size: 2.8 MB (2765674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553feeb25b7cd32c8934573fc885496b40e5ff89cf4bef4aae6d587b6d10cb2`  
		Last Modified: Tue, 15 Nov 2022 08:22:19 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8623d720f3c42dbe1854a0f481b08794fc213ed352d16b8208c1e0bc75e8fb`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 1.4 MB (1436312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c0510e8a3cd0f1b7a3ce052b46d206d04bad03bce28a3d60ed79d02f2b0c57`  
		Last Modified: Wed, 16 Nov 2022 01:36:29 GMT  
		Size: 10.2 MB (10225396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596217afd671d877e64627a6697d89fcd62931b8ecad3beccd820614a3d2cf5`  
		Last Modified: Wed, 16 Nov 2022 01:36:42 GMT  
		Size: 78.1 MB (78106018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabdd107e4fb17c5e0b38ff8aee93fa48afa5019343da9a5f945332195fa946`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.22-alpine`

```console
$ docker pull ghost@sha256:dcda6872d81dad08a1fa9c45d11b0836759fca6de897ee2ecd8f06e9c774d28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:5.22-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:839e74e0be715e1164e0286d25623233b65bec72f5c49d1653fddbc789609d74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133735107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba65fa4741d3de85fecf5dfb61d1e46809bd209088bec4cda4927748243dbb0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:31:38 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 06:31:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:31:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:31:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:31:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:31:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:31:51 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:25:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:25:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:25:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:25:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:25:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:23:52 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:25:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:25:41 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:25:41 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:25:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:25:41 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:25:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb1b25da51088e0fd1776f0b761b6d6b10d19b644e4c0d2a0e7c6d2237d8c65`  
		Last Modified: Sat, 12 Nov 2022 06:36:36 GMT  
		Size: 36.6 MB (36574826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604515c95e115c675e3e4467f77080c2aee4759272fa78161bde7a9536ef169`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 2.4 MB (2351149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bf7dff8d854e790d3475c79af59120a2f578bf057c5ed4512d19839649c41f`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d9e36250dcfd97ebc121e69a9856496b40b92ae7aa858eeff8806b81e4e9a`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 11.3 KB (11293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3f18cf69e59f39475d0dace45f0aca55c6b78bc13441a07b261bd928c76f0`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38893683f95f259b97b62421595bee0c4cdf2cbe2f4ffd4798777de70f4893d6`  
		Last Modified: Sat, 12 Nov 2022 11:30:02 GMT  
		Size: 10.2 MB (10221109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5db84843950d5baac2d64b7b859550e2611399ca90b5b81746cbe90fbe4db7`  
		Last Modified: Tue, 15 Nov 2022 01:26:50 GMT  
		Size: 80.9 MB (80949393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12c7ed583754de5cd2bfb1bcb57c3284cb0ab6c6b753e189ab7db63d9b4cb42`  
		Last Modified: Tue, 15 Nov 2022 01:26:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:0ae556437c35ee790aab65cfe9f7417201e0356da7682abcd3fcbfd92965a3d1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730cc2688da47e562d5330cadb00d4190e2cbcba37c78d2abfe3baebf4aaf6b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:59:51 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 10:48:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 10:48:42 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 10:48:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 10:48:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 10:48:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 10:48:49 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:04:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:04:43 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:04:43 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:04:43 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:05:18 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:49:26 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:59:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 02:00:03 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 02:00:04 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 02:00:04 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 02:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 02:00:04 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 02:00:04 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f611d26fd649b9911106001558a1fc88106d042a4a58f18d143f315bb9b4d`  
		Last Modified: Sat, 12 Nov 2022 11:28:47 GMT  
		Size: 35.5 MB (35511547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375aad15b0390a11efe0d2624016142a73d3d40b4d08f5f7bd4ae5a2a0ce8f4b`  
		Last Modified: Sat, 12 Nov 2022 11:28:40 GMT  
		Size: 2.4 MB (2399842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e182de8dbbe31b087dae17062287b2276c9f9505251aeeef2e23f31241cc6`  
		Last Modified: Sat, 12 Nov 2022 11:28:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8bc1a231aa404a6ade4980ed81c0ea8d471ca420441c9b9975e8771d9b9734`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a546cf8571bd364a88c8604b1f78d1ccb7e6ea476b9e6eb0a38bc2cc56771536`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 772.0 KB (771952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b890066ace05ae48e45e47baa1072b801c4eedc7c84c99cc2c977c1ecb300`  
		Last Modified: Sat, 12 Nov 2022 14:23:07 GMT  
		Size: 10.2 MB (10227843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade4e0a4ec2f548f3f3ae429a94f370b249e93a2c12eafa0f0b9b429d4090c33`  
		Last Modified: Tue, 15 Nov 2022 02:01:06 GMT  
		Size: 76.6 MB (76618482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d6a5c7c0cfee38eb3f1196a722a5e912b687d8fd92143ad67b740b02750e0e`  
		Last Modified: Tue, 15 Nov 2022 02:00:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:9ce397fd004a94e2d921db724d8a3b5a9583f547c275efd5c6ce292da89ee408
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127104574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f09e32a5d7431988116ac7a5fe5a6f42dca52b43d8b7cf8635497f40019d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 11:57:52 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 12:28:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:28:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:28:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:28:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:28:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:01:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:01:50 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:01:50 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:01:50 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:02:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:45:29 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:53:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:53:32 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:53:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:53:32 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 00:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:53:32 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:53:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7581c8bbcf3ca02b56e1a9918948b1ecc5cc42131183451ab49aa66298a1ec`  
		Last Modified: Sat, 12 Nov 2022 12:59:40 GMT  
		Size: 35.4 MB (35404696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35120aff68c6f2f54066d564e25aa456a7d9452efd293597199f383882d637a4`  
		Last Modified: Sat, 12 Nov 2022 12:59:34 GMT  
		Size: 2.4 MB (2399918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14500faf614ce3be69f3bc4ba6664fe44fbbeec08e7b61bfd42ce6fb2438aad6`  
		Last Modified: Sat, 12 Nov 2022 12:59:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98613b1b56088e4eef1b04242d4e188e2f8b077a5ea65adf0cf5ffb6b01a3a50`  
		Last Modified: Sat, 12 Nov 2022 19:16:18 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe4ed4bafa4dcfb63b31ccc68142925eaf4be440b10fc109739768021c1f49`  
		Last Modified: Sat, 12 Nov 2022 19:16:19 GMT  
		Size: 704.7 KB (704659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5a19c40ad574aba78b769bb4ab0e8cbf695607710abb22f2b58d83087e2425`  
		Last Modified: Sat, 12 Nov 2022 19:16:23 GMT  
		Size: 10.2 MB (10223784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88b7f8a0c682fc0fb671afeaf1e7ee84f0e4e7bbbe47ebb55a15b023be2fdf`  
		Last Modified: Tue, 15 Nov 2022 00:55:45 GMT  
		Size: 75.9 MB (75940925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a41741ce8e0495a1e872512ccb3d52f4a24677d4102ab0ddcec7c160e53e0`  
		Last Modified: Tue, 15 Nov 2022 00:55:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:00b7db4c7a9bf160965498a023ad445f3bd59008c44644ae40e3685b2f495b64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141137165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5520e3ef968d5d21f55d7e04e19dc45be48e6c3a21f7d305672d39be722957c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:35:18 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 07:56:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 07:56:29 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 07:56:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 07:56:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:56:34 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:28:42 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:28:42 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:52:10 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:56:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:56:44 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:56:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:56:44 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:56:45 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:56:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28d7a0466a25c2824be774476f9c384891186b778c555fcd8cb70af320542ed`  
		Last Modified: Sat, 12 Nov 2022 08:15:29 GMT  
		Size: 36.4 MB (36428230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9597b1f237244220e9b5a52e75a0dc0f83031769f7549714f054f9af171e9e8`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 2.4 MB (2409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b006997bfe605f7d900583d90ddb61607a413baab97cea3d9b1154bfffc647`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96d881df569f57ca62d15673dcda76415a92994a1f1529aa3ec29945b9fc3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 11.1 KB (11097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da976d62d65f9b3862540036123d404465e8c65071532e9c00aa448b828c9f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 826.3 KB (826332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22c77cb9064d92dde89b1d391cd64160dac54c1885014df2384a35ac3a2ea3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:03 GMT  
		Size: 10.2 MB (10220636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd9457bd3eeb7afe3a047c7f0020c445979cd618eddde7482db65d1d5668513`  
		Last Modified: Tue, 15 Nov 2022 01:57:51 GMT  
		Size: 88.5 MB (88532795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3fd9b068511adc832a6bb38c60f4c321942c249bb31bfd179b199855820b42`  
		Last Modified: Tue, 15 Nov 2022 01:57:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.22.10`

```console
$ docker pull ghost@sha256:8b755f1acec31e63c8575a57fba0ff5cb5201ea858a4e9c2ad275bed9002b293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:5.22.10` - linux; amd64

```console
$ docker pull ghost@sha256:d7dc14254fd5b6bcc96d8a45fa5ab054301fdc2c62a8570a2da0fc0c7163f7bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161548556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001188daca9de3e0d946e910a97f19f2931348014b0450df3b099ed453c1ca78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:23:13 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 13:23:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:23:36 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:23:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:23:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:23:48 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:29:40 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:29:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:29:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:29:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:30:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 23:31:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:31:54 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:31:54 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:31:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:31:55 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:31:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf4d46bb2489b83c7602534e5a2651218fd890a70cb89e67f6905c82e41519`  
		Last Modified: Tue, 15 Nov 2022 13:33:34 GMT  
		Size: 35.5 MB (35459473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e3331ed6131ec5f8247e6c10a2cf1bfe5decf0ea27caf108da39bf2acc8640`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 2.8 MB (2764146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec19194f61cd61071c240ceb80b7bc7253268a781e4b1867ebbd561c38d6c5`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72c90f807760e639efc513b89a178ebc89b9f997b3b1d9377504c4f73fcdf75`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 1.4 MB (1449283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea25c46896f120f002dd87c9998cebabbbbdb49a181c8257baac42ed90a2fc`  
		Last Modified: Tue, 15 Nov 2022 23:34:49 GMT  
		Size: 10.2 MB (10221363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdb760963cb9640c173e3d3cf19be1fffa7c6b74bb933e287e0a06c0950a2a5`  
		Last Modified: Tue, 15 Nov 2022 23:35:03 GMT  
		Size: 80.2 MB (80236481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f277ce8b6640231de36cd96b2dd3774fc89c3ec080711c2c1b51eb918fd1a4`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1287661a59dd3f5ab9f7b32d3d6fafefd27c9516c823ecd6a75d70814cda3591
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165783911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e481eae5257a93529264d3c19f279dc7de887154272f5e02bbd226183a30fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 00:14:01 GMT
ENV NODE_VERSION=16.18.1
# Wed, 09 Nov 2022 00:14:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 00:14:25 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 00:14:39 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 00:14:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 00:14:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 00:14:39 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:36:34 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:36:47 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:36:47 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:37:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:39:59 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:45:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:45:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:45:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:45:21 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 00:45:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:45:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:45:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea8153e91aead518fb126da6eaa6a5537bab1e59ccf5158259758e7eb52023`  
		Last Modified: Wed, 09 Nov 2022 01:31:43 GMT  
		Size: 32.7 MB (32674064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347d8b382bcc282f50e1852663f7bb13e02fcb73c5aefd2941d560301c77513`  
		Last Modified: Wed, 09 Nov 2022 01:31:37 GMT  
		Size: 2.8 MB (2754357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad09949a32d06a6c9bcdda5c737a82fe18c5150f06ce1f8d3748775844f6ebcc`  
		Last Modified: Wed, 09 Nov 2022 01:31:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd827919251e7f3fd55d8971a48ac80d30260a48bb44aaabc96aa3107a0be126`  
		Last Modified: Wed, 09 Nov 2022 03:01:55 GMT  
		Size: 1.4 MB (1401933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b582ead2fdbe8a32cf94e60cbb709733a8fe6cfcef9c123a01146c628de9f0`  
		Last Modified: Wed, 09 Nov 2022 03:01:59 GMT  
		Size: 10.2 MB (10222051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e794c1499dcd232c94c502ae0fdf10cd0bfb996c1b8606365ee1efe5de6a56`  
		Last Modified: Tue, 15 Nov 2022 00:55:01 GMT  
		Size: 92.1 MB (92147067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d89048947e4277b5c42b31a44a2e499e87d964ae6d6984644c2b480a6c64b3`  
		Last Modified: Tue, 15 Nov 2022 00:54:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d353e6327748fe7f3363f0d61fd592cddd8b358cb13b2f276c837b78a7f1b142
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169075352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8643932b495135341e6d425cb9a2a5542064fb78a4ee04c98845e04e663801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:45:59 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 06:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:46:18 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:46:27 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:46:27 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:46:28 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:14:33 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:14:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:14:44 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:14:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:14:57 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 22:18:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:18:47 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:18:47 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:18:47 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:18:48 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:18:48 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6818cad41f1d340b619ad94fcdeba483b7d959319c2b05023bc3b3d032dd9fe`  
		Last Modified: Tue, 15 Nov 2022 06:55:57 GMT  
		Size: 35.7 MB (35700928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec1e2eaae6f47edd60f65027854a48a59d04160e1f602f9612f282bed16bfb`  
		Last Modified: Tue, 15 Nov 2022 06:55:54 GMT  
		Size: 2.8 MB (2763892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8318b016de3ae2c2e9ea562bcdef9e07680e94e75a09ccb997bba3a940c82`  
		Last Modified: Tue, 15 Nov 2022 06:55:53 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37965a6a28429507a0443198d6fb57eb92bf02b4825ffe3050533544267ed328`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 1.4 MB (1385222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d2cdfd6571f64df92ce24977dcfda34fd83f1badfd1b7e3a0d84746d9f967`  
		Last Modified: Tue, 15 Nov 2022 22:21:28 GMT  
		Size: 10.2 MB (10220713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1ed3bef567b2ff43af194597b8f0387ad3d62ac40c1476ede48fecb4c30ac`  
		Last Modified: Tue, 15 Nov 2022 22:21:41 GMT  
		Size: 88.9 MB (88938811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a980f49926890e46de7153fd1e518c6970381fb09e6cec2c10d7e4ece030e96`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10` - linux; ppc64le

```console
$ docker pull ghost@sha256:cfa5bacef385f8968406e20d27059d8e073ecddf5f5a6e32a2810ef7845924ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165351765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d32af16b262d202f6e92061a74f8e48459bfb471f6399c09512bfbc700342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:07:48 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 18:08:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:08:29 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:08:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:08:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:08:57 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:16:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:16:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:16:24 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:16:24 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:16:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 19:27:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:27:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:27:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:27:22 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:27:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:27:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc704eecace49db0b3b527128a9c246649c5b01952bc85cd0cb619ba871036`  
		Last Modified: Tue, 15 Nov 2022 18:19:51 GMT  
		Size: 37.5 MB (37514111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3448e957aebe054316bec55eeb7221f6c31178f34d53401774228b5168e7c0b`  
		Last Modified: Tue, 15 Nov 2022 18:19:42 GMT  
		Size: 2.8 MB (2764077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e5af461d4b8e4bc212e2164deb20339ce80e9777e0702fb326ad1df21c5e8f`  
		Last Modified: Tue, 15 Nov 2022 18:19:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96460bc859bb7bc52cc87115370348e9cbb870e4a9f31db19ebfca0ee700330`  
		Last Modified: Tue, 15 Nov 2022 19:37:47 GMT  
		Size: 1.4 MB (1369026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a06b8efc7b2887731416d83a3d4bf5dac060651aa86ec09c724aacef8a1a56`  
		Last Modified: Tue, 15 Nov 2022 19:37:52 GMT  
		Size: 10.2 MB (10227513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cc7197a5eeb2c64335942f83bacd788eceab7a3fe59bbf1de22ec37020e313`  
		Last Modified: Tue, 15 Nov 2022 19:38:18 GMT  
		Size: 78.2 MB (78186722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcb4f5472c1392866505e519ff2726624578a41dd12dc955876f2f479ecd04`  
		Last Modified: Tue, 15 Nov 2022 19:37:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10` - linux; s390x

```console
$ docker pull ghost@sha256:e49397a5850f441fb801a76b0a5c81a4ba36a003a26d920af55a42847da1dac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157552613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18d55cd8f8f97f9411189baf6f322687c8c6f01e998a0069796bade80e917e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:11:20 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 08:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:12:01 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:12:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:12:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:12:23 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:11:05 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:11:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:11:30 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:11:31 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:12:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:12:12 GMT
ENV GHOST_VERSION=5.22.10
# Wed, 16 Nov 2022 01:20:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:21:15 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:21:15 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:21:16 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:21:17 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:21:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fda3a1e3ada00d249bc778488a797425cf7cd8050e77843ebeb0f5ea62f224`  
		Last Modified: Tue, 15 Nov 2022 08:22:25 GMT  
		Size: 35.4 MB (35370246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d9e5094e9573f77781bb698c378fad5e70b19e7980e000ecbfe5bbf2e5a500`  
		Last Modified: Tue, 15 Nov 2022 08:22:20 GMT  
		Size: 2.8 MB (2765674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553feeb25b7cd32c8934573fc885496b40e5ff89cf4bef4aae6d587b6d10cb2`  
		Last Modified: Tue, 15 Nov 2022 08:22:19 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8623d720f3c42dbe1854a0f481b08794fc213ed352d16b8208c1e0bc75e8fb`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 1.4 MB (1436312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c0510e8a3cd0f1b7a3ce052b46d206d04bad03bce28a3d60ed79d02f2b0c57`  
		Last Modified: Wed, 16 Nov 2022 01:36:29 GMT  
		Size: 10.2 MB (10225396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596217afd671d877e64627a6697d89fcd62931b8ecad3beccd820614a3d2cf5`  
		Last Modified: Wed, 16 Nov 2022 01:36:42 GMT  
		Size: 78.1 MB (78106018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabdd107e4fb17c5e0b38ff8aee93fa48afa5019343da9a5f945332195fa946`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.22.10-alpine`

```console
$ docker pull ghost@sha256:dcda6872d81dad08a1fa9c45d11b0836759fca6de897ee2ecd8f06e9c774d28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:5.22.10-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:839e74e0be715e1164e0286d25623233b65bec72f5c49d1653fddbc789609d74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133735107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba65fa4741d3de85fecf5dfb61d1e46809bd209088bec4cda4927748243dbb0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:31:38 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 06:31:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:31:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:31:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:31:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:31:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:31:51 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:25:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:25:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:25:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:25:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:25:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:23:52 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:25:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:25:41 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:25:41 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:25:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:25:41 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:25:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb1b25da51088e0fd1776f0b761b6d6b10d19b644e4c0d2a0e7c6d2237d8c65`  
		Last Modified: Sat, 12 Nov 2022 06:36:36 GMT  
		Size: 36.6 MB (36574826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604515c95e115c675e3e4467f77080c2aee4759272fa78161bde7a9536ef169`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 2.4 MB (2351149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bf7dff8d854e790d3475c79af59120a2f578bf057c5ed4512d19839649c41f`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d9e36250dcfd97ebc121e69a9856496b40b92ae7aa858eeff8806b81e4e9a`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 11.3 KB (11293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3f18cf69e59f39475d0dace45f0aca55c6b78bc13441a07b261bd928c76f0`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38893683f95f259b97b62421595bee0c4cdf2cbe2f4ffd4798777de70f4893d6`  
		Last Modified: Sat, 12 Nov 2022 11:30:02 GMT  
		Size: 10.2 MB (10221109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5db84843950d5baac2d64b7b859550e2611399ca90b5b81746cbe90fbe4db7`  
		Last Modified: Tue, 15 Nov 2022 01:26:50 GMT  
		Size: 80.9 MB (80949393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12c7ed583754de5cd2bfb1bcb57c3284cb0ab6c6b753e189ab7db63d9b4cb42`  
		Last Modified: Tue, 15 Nov 2022 01:26:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:0ae556437c35ee790aab65cfe9f7417201e0356da7682abcd3fcbfd92965a3d1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730cc2688da47e562d5330cadb00d4190e2cbcba37c78d2abfe3baebf4aaf6b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:59:51 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 10:48:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 10:48:42 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 10:48:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 10:48:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 10:48:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 10:48:49 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:04:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:04:43 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:04:43 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:04:43 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:05:18 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:49:26 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:59:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 02:00:03 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 02:00:04 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 02:00:04 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 02:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 02:00:04 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 02:00:04 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f611d26fd649b9911106001558a1fc88106d042a4a58f18d143f315bb9b4d`  
		Last Modified: Sat, 12 Nov 2022 11:28:47 GMT  
		Size: 35.5 MB (35511547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375aad15b0390a11efe0d2624016142a73d3d40b4d08f5f7bd4ae5a2a0ce8f4b`  
		Last Modified: Sat, 12 Nov 2022 11:28:40 GMT  
		Size: 2.4 MB (2399842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e182de8dbbe31b087dae17062287b2276c9f9505251aeeef2e23f31241cc6`  
		Last Modified: Sat, 12 Nov 2022 11:28:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8bc1a231aa404a6ade4980ed81c0ea8d471ca420441c9b9975e8771d9b9734`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a546cf8571bd364a88c8604b1f78d1ccb7e6ea476b9e6eb0a38bc2cc56771536`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 772.0 KB (771952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b890066ace05ae48e45e47baa1072b801c4eedc7c84c99cc2c977c1ecb300`  
		Last Modified: Sat, 12 Nov 2022 14:23:07 GMT  
		Size: 10.2 MB (10227843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade4e0a4ec2f548f3f3ae429a94f370b249e93a2c12eafa0f0b9b429d4090c33`  
		Last Modified: Tue, 15 Nov 2022 02:01:06 GMT  
		Size: 76.6 MB (76618482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d6a5c7c0cfee38eb3f1196a722a5e912b687d8fd92143ad67b740b02750e0e`  
		Last Modified: Tue, 15 Nov 2022 02:00:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:9ce397fd004a94e2d921db724d8a3b5a9583f547c275efd5c6ce292da89ee408
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127104574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f09e32a5d7431988116ac7a5fe5a6f42dca52b43d8b7cf8635497f40019d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 11:57:52 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 12:28:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:28:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:28:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:28:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:28:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:01:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:01:50 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:01:50 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:01:50 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:02:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:45:29 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:53:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:53:32 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:53:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:53:32 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 00:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:53:32 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:53:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7581c8bbcf3ca02b56e1a9918948b1ecc5cc42131183451ab49aa66298a1ec`  
		Last Modified: Sat, 12 Nov 2022 12:59:40 GMT  
		Size: 35.4 MB (35404696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35120aff68c6f2f54066d564e25aa456a7d9452efd293597199f383882d637a4`  
		Last Modified: Sat, 12 Nov 2022 12:59:34 GMT  
		Size: 2.4 MB (2399918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14500faf614ce3be69f3bc4ba6664fe44fbbeec08e7b61bfd42ce6fb2438aad6`  
		Last Modified: Sat, 12 Nov 2022 12:59:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98613b1b56088e4eef1b04242d4e188e2f8b077a5ea65adf0cf5ffb6b01a3a50`  
		Last Modified: Sat, 12 Nov 2022 19:16:18 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe4ed4bafa4dcfb63b31ccc68142925eaf4be440b10fc109739768021c1f49`  
		Last Modified: Sat, 12 Nov 2022 19:16:19 GMT  
		Size: 704.7 KB (704659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5a19c40ad574aba78b769bb4ab0e8cbf695607710abb22f2b58d83087e2425`  
		Last Modified: Sat, 12 Nov 2022 19:16:23 GMT  
		Size: 10.2 MB (10223784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88b7f8a0c682fc0fb671afeaf1e7ee84f0e4e7bbbe47ebb55a15b023be2fdf`  
		Last Modified: Tue, 15 Nov 2022 00:55:45 GMT  
		Size: 75.9 MB (75940925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a41741ce8e0495a1e872512ccb3d52f4a24677d4102ab0ddcec7c160e53e0`  
		Last Modified: Tue, 15 Nov 2022 00:55:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.22.10-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:00b7db4c7a9bf160965498a023ad445f3bd59008c44644ae40e3685b2f495b64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141137165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5520e3ef968d5d21f55d7e04e19dc45be48e6c3a21f7d305672d39be722957c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:35:18 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 07:56:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 07:56:29 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 07:56:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 07:56:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:56:34 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:28:42 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:28:42 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:52:10 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:56:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:56:44 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:56:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:56:44 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:56:45 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:56:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28d7a0466a25c2824be774476f9c384891186b778c555fcd8cb70af320542ed`  
		Last Modified: Sat, 12 Nov 2022 08:15:29 GMT  
		Size: 36.4 MB (36428230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9597b1f237244220e9b5a52e75a0dc0f83031769f7549714f054f9af171e9e8`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 2.4 MB (2409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b006997bfe605f7d900583d90ddb61607a413baab97cea3d9b1154bfffc647`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96d881df569f57ca62d15673dcda76415a92994a1f1529aa3ec29945b9fc3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 11.1 KB (11097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da976d62d65f9b3862540036123d404465e8c65071532e9c00aa448b828c9f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 826.3 KB (826332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22c77cb9064d92dde89b1d391cd64160dac54c1885014df2384a35ac3a2ea3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:03 GMT  
		Size: 10.2 MB (10220636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd9457bd3eeb7afe3a047c7f0020c445979cd618eddde7482db65d1d5668513`  
		Last Modified: Tue, 15 Nov 2022 01:57:51 GMT  
		Size: 88.5 MB (88532795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3fd9b068511adc832a6bb38c60f4c321942c249bb31bfd179b199855820b42`  
		Last Modified: Tue, 15 Nov 2022 01:57:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:dcda6872d81dad08a1fa9c45d11b0836759fca6de897ee2ecd8f06e9c774d28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:839e74e0be715e1164e0286d25623233b65bec72f5c49d1653fddbc789609d74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133735107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba65fa4741d3de85fecf5dfb61d1e46809bd209088bec4cda4927748243dbb0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:31:38 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 06:31:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 06:31:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 06:31:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 06:31:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:31:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:31:51 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:25:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:25:26 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:25:26 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:25:26 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:25:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:25:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:23:52 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:25:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:25:41 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:25:41 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:25:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:25:41 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:25:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb1b25da51088e0fd1776f0b761b6d6b10d19b644e4c0d2a0e7c6d2237d8c65`  
		Last Modified: Sat, 12 Nov 2022 06:36:36 GMT  
		Size: 36.6 MB (36574826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604515c95e115c675e3e4467f77080c2aee4759272fa78161bde7a9536ef169`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 2.4 MB (2351149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bf7dff8d854e790d3475c79af59120a2f578bf057c5ed4512d19839649c41f`  
		Last Modified: Sat, 12 Nov 2022 06:36:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d9e36250dcfd97ebc121e69a9856496b40b92ae7aa858eeff8806b81e4e9a`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 11.3 KB (11293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3f18cf69e59f39475d0dace45f0aca55c6b78bc13441a07b261bd928c76f0`  
		Last Modified: Sat, 12 Nov 2022 11:29:59 GMT  
		Size: 820.1 KB (820068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38893683f95f259b97b62421595bee0c4cdf2cbe2f4ffd4798777de70f4893d6`  
		Last Modified: Sat, 12 Nov 2022 11:30:02 GMT  
		Size: 10.2 MB (10221109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5db84843950d5baac2d64b7b859550e2611399ca90b5b81746cbe90fbe4db7`  
		Last Modified: Tue, 15 Nov 2022 01:26:50 GMT  
		Size: 80.9 MB (80949393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12c7ed583754de5cd2bfb1bcb57c3284cb0ab6c6b753e189ab7db63d9b4cb42`  
		Last Modified: Tue, 15 Nov 2022 01:26:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:0ae556437c35ee790aab65cfe9f7417201e0356da7682abcd3fcbfd92965a3d1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730cc2688da47e562d5330cadb00d4190e2cbcba37c78d2abfe3baebf4aaf6b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:59:51 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 10:48:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 10:48:42 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 10:48:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 10:48:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 10:48:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 10:48:49 GMT
CMD ["node"]
# Sat, 12 Nov 2022 14:04:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 14:04:43 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 14:04:43 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 14:04:43 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 14:05:18 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 14:05:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:49:26 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:59:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 02:00:03 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 02:00:04 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 02:00:04 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 02:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 02:00:04 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 02:00:04 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f611d26fd649b9911106001558a1fc88106d042a4a58f18d143f315bb9b4d`  
		Last Modified: Sat, 12 Nov 2022 11:28:47 GMT  
		Size: 35.5 MB (35511547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375aad15b0390a11efe0d2624016142a73d3d40b4d08f5f7bd4ae5a2a0ce8f4b`  
		Last Modified: Sat, 12 Nov 2022 11:28:40 GMT  
		Size: 2.4 MB (2399842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e182de8dbbe31b087dae17062287b2276c9f9505251aeeef2e23f31241cc6`  
		Last Modified: Sat, 12 Nov 2022 11:28:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8bc1a231aa404a6ade4980ed81c0ea8d471ca420441c9b9975e8771d9b9734`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 11.0 KB (10998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a546cf8571bd364a88c8604b1f78d1ccb7e6ea476b9e6eb0a38bc2cc56771536`  
		Last Modified: Sat, 12 Nov 2022 14:23:03 GMT  
		Size: 772.0 KB (771952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b890066ace05ae48e45e47baa1072b801c4eedc7c84c99cc2c977c1ecb300`  
		Last Modified: Sat, 12 Nov 2022 14:23:07 GMT  
		Size: 10.2 MB (10227843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade4e0a4ec2f548f3f3ae429a94f370b249e93a2c12eafa0f0b9b429d4090c33`  
		Last Modified: Tue, 15 Nov 2022 02:01:06 GMT  
		Size: 76.6 MB (76618482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d6a5c7c0cfee38eb3f1196a722a5e912b687d8fd92143ad67b740b02750e0e`  
		Last Modified: Tue, 15 Nov 2022 02:00:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:9ce397fd004a94e2d921db724d8a3b5a9583f547c275efd5c6ce292da89ee408
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127104574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f09e32a5d7431988116ac7a5fe5a6f42dca52b43d8b7cf8635497f40019d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 11:57:52 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 12:28:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 12:28:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 12:28:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 12:28:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:28:11 GMT
CMD ["node"]
# Sat, 12 Nov 2022 19:01:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 19:01:50 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 19:01:50 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 19:01:50 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 19:02:09 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 19:02:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:45:29 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:53:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:53:32 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:53:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:53:32 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 00:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:53:32 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:53:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7581c8bbcf3ca02b56e1a9918948b1ecc5cc42131183451ab49aa66298a1ec`  
		Last Modified: Sat, 12 Nov 2022 12:59:40 GMT  
		Size: 35.4 MB (35404696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35120aff68c6f2f54066d564e25aa456a7d9452efd293597199f383882d637a4`  
		Last Modified: Sat, 12 Nov 2022 12:59:34 GMT  
		Size: 2.4 MB (2399918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14500faf614ce3be69f3bc4ba6664fe44fbbeec08e7b61bfd42ce6fb2438aad6`  
		Last Modified: Sat, 12 Nov 2022 12:59:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98613b1b56088e4eef1b04242d4e188e2f8b077a5ea65adf0cf5ffb6b01a3a50`  
		Last Modified: Sat, 12 Nov 2022 19:16:18 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe4ed4bafa4dcfb63b31ccc68142925eaf4be440b10fc109739768021c1f49`  
		Last Modified: Sat, 12 Nov 2022 19:16:19 GMT  
		Size: 704.7 KB (704659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5a19c40ad574aba78b769bb4ab0e8cbf695607710abb22f2b58d83087e2425`  
		Last Modified: Sat, 12 Nov 2022 19:16:23 GMT  
		Size: 10.2 MB (10223784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88b7f8a0c682fc0fb671afeaf1e7ee84f0e4e7bbbe47ebb55a15b023be2fdf`  
		Last Modified: Tue, 15 Nov 2022 00:55:45 GMT  
		Size: 75.9 MB (75940925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a41741ce8e0495a1e872512ccb3d52f4a24677d4102ab0ddcec7c160e53e0`  
		Last Modified: Tue, 15 Nov 2022 00:55:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:00b7db4c7a9bf160965498a023ad445f3bd59008c44644ae40e3685b2f495b64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141137165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5520e3ef968d5d21f55d7e04e19dc45be48e6c3a21f7d305672d39be722957c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:35:18 GMT
ENV NODE_VERSION=16.18.1
# Sat, 12 Nov 2022 07:56:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="ba6f8e66b23518ff4ff465814f781fd48b196a1cd77a9942ca5c7857715253a9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 12 Nov 2022 07:56:29 GMT
ENV YARN_VERSION=1.22.19
# Sat, 12 Nov 2022 07:56:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 12 Nov 2022 07:56:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:56:34 GMT
CMD ["node"]
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 11:28:41 GMT
RUN apk add --no-cache 		bash
# Sat, 12 Nov 2022 11:28:42 GMT
ENV NODE_ENV=production
# Sat, 12 Nov 2022 11:28:42 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Sat, 12 Nov 2022 11:28:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 12 Nov 2022 11:28:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 01:52:10 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 01:56:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 01:56:44 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 01:56:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 01:56:44 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 15 Nov 2022 01:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 01:56:45 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 01:56:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28d7a0466a25c2824be774476f9c384891186b778c555fcd8cb70af320542ed`  
		Last Modified: Sat, 12 Nov 2022 08:15:29 GMT  
		Size: 36.4 MB (36428230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9597b1f237244220e9b5a52e75a0dc0f83031769f7549714f054f9af171e9e8`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 2.4 MB (2409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b006997bfe605f7d900583d90ddb61607a413baab97cea3d9b1154bfffc647`  
		Last Modified: Sat, 12 Nov 2022 08:15:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96d881df569f57ca62d15673dcda76415a92994a1f1529aa3ec29945b9fc3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 11.1 KB (11097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da976d62d65f9b3862540036123d404465e8c65071532e9c00aa448b828c9f`  
		Last Modified: Sat, 12 Nov 2022 11:36:01 GMT  
		Size: 826.3 KB (826332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22c77cb9064d92dde89b1d391cd64160dac54c1885014df2384a35ac3a2ea3f`  
		Last Modified: Sat, 12 Nov 2022 11:36:03 GMT  
		Size: 10.2 MB (10220636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd9457bd3eeb7afe3a047c7f0020c445979cd618eddde7482db65d1d5668513`  
		Last Modified: Tue, 15 Nov 2022 01:57:51 GMT  
		Size: 88.5 MB (88532795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3fd9b068511adc832a6bb38c60f4c321942c249bb31bfd179b199855820b42`  
		Last Modified: Tue, 15 Nov 2022 01:57:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:8b755f1acec31e63c8575a57fba0ff5cb5201ea858a4e9c2ad275bed9002b293
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
$ docker pull ghost@sha256:d7dc14254fd5b6bcc96d8a45fa5ab054301fdc2c62a8570a2da0fc0c7163f7bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161548556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001188daca9de3e0d946e910a97f19f2931348014b0450df3b099ed453c1ca78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:18:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 13:23:13 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 13:23:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 13:23:36 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 13:23:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 13:23:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:23:48 GMT
CMD ["node"]
# Tue, 15 Nov 2022 23:29:40 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 23:29:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 23:29:54 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 23:29:54 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 23:30:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 23:30:13 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 23:31:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 23:31:54 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 23:31:54 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 23:31:55 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 23:31:55 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 23:31:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d5778cf5877061cef5d01039c5f979ed9a17d88794e75e322d84071c8efc9`  
		Last Modified: Tue, 15 Nov 2022 13:29:51 GMT  
		Size: 4.2 KB (4183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf4d46bb2489b83c7602534e5a2651218fd890a70cb89e67f6905c82e41519`  
		Last Modified: Tue, 15 Nov 2022 13:33:34 GMT  
		Size: 35.5 MB (35459473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e3331ed6131ec5f8247e6c10a2cf1bfe5decf0ea27caf108da39bf2acc8640`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 2.8 MB (2764146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec19194f61cd61071c240ceb80b7bc7253268a781e4b1867ebbd561c38d6c5`  
		Last Modified: Tue, 15 Nov 2022 13:33:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72c90f807760e639efc513b89a178ebc89b9f997b3b1d9377504c4f73fcdf75`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 1.4 MB (1449283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea25c46896f120f002dd87c9998cebabbbbdb49a181c8257baac42ed90a2fc`  
		Last Modified: Tue, 15 Nov 2022 23:34:49 GMT  
		Size: 10.2 MB (10221363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdb760963cb9640c173e3d3cf19be1fffa7c6b74bb933e287e0a06c0950a2a5`  
		Last Modified: Tue, 15 Nov 2022 23:35:03 GMT  
		Size: 80.2 MB (80236481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f277ce8b6640231de36cd96b2dd3774fc89c3ec080711c2c1b51eb918fd1a4`  
		Last Modified: Tue, 15 Nov 2022 23:34:46 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1287661a59dd3f5ab9f7b32d3d6fafefd27c9516c823ecd6a75d70814cda3591
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165783911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e481eae5257a93529264d3c19f279dc7de887154272f5e02bbd226183a30fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:27:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 09 Nov 2022 00:14:01 GMT
ENV NODE_VERSION=16.18.1
# Wed, 09 Nov 2022 00:14:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 09 Nov 2022 00:14:25 GMT
ENV YARN_VERSION=1.22.19
# Wed, 09 Nov 2022 00:14:39 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 09 Nov 2022 00:14:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 09 Nov 2022 00:14:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Nov 2022 00:14:39 GMT
CMD ["node"]
# Wed, 09 Nov 2022 02:36:34 GMT
ENV GOSU_VERSION=1.12
# Wed, 09 Nov 2022 02:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 09 Nov 2022 02:36:47 GMT
ENV NODE_ENV=production
# Wed, 09 Nov 2022 02:36:47 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 09 Nov 2022 02:37:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 09 Nov 2022 02:37:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 00:39:59 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 00:45:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 00:45:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 00:45:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 00:45:21 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 00:45:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 00:45:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 00:45:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d906b066769ac613299a88db9aa972fc607c561af85743f4ab8b9630d0fc67c`  
		Last Modified: Tue, 25 Oct 2022 21:33:28 GMT  
		Size: 4.1 KB (4144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea8153e91aead518fb126da6eaa6a5537bab1e59ccf5158259758e7eb52023`  
		Last Modified: Wed, 09 Nov 2022 01:31:43 GMT  
		Size: 32.7 MB (32674064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347d8b382bcc282f50e1852663f7bb13e02fcb73c5aefd2941d560301c77513`  
		Last Modified: Wed, 09 Nov 2022 01:31:37 GMT  
		Size: 2.8 MB (2754357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad09949a32d06a6c9bcdda5c737a82fe18c5150f06ce1f8d3748775844f6ebcc`  
		Last Modified: Wed, 09 Nov 2022 01:31:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd827919251e7f3fd55d8971a48ac80d30260a48bb44aaabc96aa3107a0be126`  
		Last Modified: Wed, 09 Nov 2022 03:01:55 GMT  
		Size: 1.4 MB (1401933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b582ead2fdbe8a32cf94e60cbb709733a8fe6cfcef9c123a01146c628de9f0`  
		Last Modified: Wed, 09 Nov 2022 03:01:59 GMT  
		Size: 10.2 MB (10222051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e794c1499dcd232c94c502ae0fdf10cd0bfb996c1b8606365ee1efe5de6a56`  
		Last Modified: Tue, 15 Nov 2022 00:55:01 GMT  
		Size: 92.1 MB (92147067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d89048947e4277b5c42b31a44a2e499e87d964ae6d6984644c2b480a6c64b3`  
		Last Modified: Tue, 15 Nov 2022 00:54:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d353e6327748fe7f3363f0d61fd592cddd8b358cb13b2f276c837b78a7f1b142
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169075352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8643932b495135341e6d425cb9a2a5542064fb78a4ee04c98845e04e663801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:41:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 06:45:59 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 06:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 06:46:18 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 06:46:27 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 06:46:27 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:46:28 GMT
CMD ["node"]
# Tue, 15 Nov 2022 22:14:33 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 22:14:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 22:14:44 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 22:14:44 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 22:14:57 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 22:14:57 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 22:18:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 22:18:47 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 22:18:47 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 22:18:47 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 22:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 22:18:48 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 22:18:48 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d29e2e4538c03db5863875eadbb277774d504488b51b291440654caf3516`  
		Last Modified: Tue, 15 Nov 2022 06:52:16 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6818cad41f1d340b619ad94fcdeba483b7d959319c2b05023bc3b3d032dd9fe`  
		Last Modified: Tue, 15 Nov 2022 06:55:57 GMT  
		Size: 35.7 MB (35700928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec1e2eaae6f47edd60f65027854a48a59d04160e1f602f9612f282bed16bfb`  
		Last Modified: Tue, 15 Nov 2022 06:55:54 GMT  
		Size: 2.8 MB (2763892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8318b016de3ae2c2e9ea562bcdef9e07680e94e75a09ccb997bba3a940c82`  
		Last Modified: Tue, 15 Nov 2022 06:55:53 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37965a6a28429507a0443198d6fb57eb92bf02b4825ffe3050533544267ed328`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 1.4 MB (1385222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d2cdfd6571f64df92ce24977dcfda34fd83f1badfd1b7e3a0d84746d9f967`  
		Last Modified: Tue, 15 Nov 2022 22:21:28 GMT  
		Size: 10.2 MB (10220713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1ed3bef567b2ff43af194597b8f0387ad3d62ac40c1476ede48fecb4c30ac`  
		Last Modified: Tue, 15 Nov 2022 22:21:41 GMT  
		Size: 88.9 MB (88938811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a980f49926890e46de7153fd1e518c6970381fb09e6cec2c10d7e4ece030e96`  
		Last Modified: Tue, 15 Nov 2022 22:21:26 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:cfa5bacef385f8968406e20d27059d8e073ecddf5f5a6e32a2810ef7845924ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165351765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2d32af16b262d202f6e92061a74f8e48459bfb471f6399c09512bfbc700342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:03:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 18:07:48 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 18:08:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 18:08:29 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 18:08:56 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 18:08:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 18:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:08:57 GMT
CMD ["node"]
# Tue, 15 Nov 2022 19:16:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 15 Nov 2022 19:16:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 19:16:24 GMT
ENV NODE_ENV=production
# Tue, 15 Nov 2022 19:16:24 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Tue, 15 Nov 2022 19:16:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 15 Nov 2022 19:16:56 GMT
ENV GHOST_VERSION=5.22.10
# Tue, 15 Nov 2022 19:27:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 15 Nov 2022 19:27:21 GMT
WORKDIR /var/lib/ghost
# Tue, 15 Nov 2022 19:27:21 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 15 Nov 2022 19:27:22 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Tue, 15 Nov 2022 19:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 19:27:22 GMT
EXPOSE 2368
# Tue, 15 Nov 2022 19:27:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8444d74ef5cb74949f816b2096cc3e374a2421874f4c661019d9aa2d9f302`  
		Last Modified: Tue, 15 Nov 2022 18:16:18 GMT  
		Size: 4.2 KB (4181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc704eecace49db0b3b527128a9c246649c5b01952bc85cd0cb619ba871036`  
		Last Modified: Tue, 15 Nov 2022 18:19:51 GMT  
		Size: 37.5 MB (37514111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3448e957aebe054316bec55eeb7221f6c31178f34d53401774228b5168e7c0b`  
		Last Modified: Tue, 15 Nov 2022 18:19:42 GMT  
		Size: 2.8 MB (2764077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e5af461d4b8e4bc212e2164deb20339ce80e9777e0702fb326ad1df21c5e8f`  
		Last Modified: Tue, 15 Nov 2022 18:19:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96460bc859bb7bc52cc87115370348e9cbb870e4a9f31db19ebfca0ee700330`  
		Last Modified: Tue, 15 Nov 2022 19:37:47 GMT  
		Size: 1.4 MB (1369026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a06b8efc7b2887731416d83a3d4bf5dac060651aa86ec09c724aacef8a1a56`  
		Last Modified: Tue, 15 Nov 2022 19:37:52 GMT  
		Size: 10.2 MB (10227513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cc7197a5eeb2c64335942f83bacd788eceab7a3fe59bbf1de22ec37020e313`  
		Last Modified: Tue, 15 Nov 2022 19:38:18 GMT  
		Size: 78.2 MB (78186722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcb4f5472c1392866505e519ff2726624578a41dd12dc955876f2f479ecd04`  
		Last Modified: Tue, 15 Nov 2022 19:37:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:e49397a5850f441fb801a76b0a5c81a4ba36a003a26d920af55a42847da1dac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157552613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18d55cd8f8f97f9411189baf6f322687c8c6f01e998a0069796bade80e917e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 08:06:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 15 Nov 2022 08:11:20 GMT
ENV NODE_VERSION=16.18.1
# Tue, 15 Nov 2022 08:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Tue, 15 Nov 2022 08:12:01 GMT
ENV YARN_VERSION=1.22.19
# Tue, 15 Nov 2022 08:12:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Tue, 15 Nov 2022 08:12:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:12:23 GMT
CMD ["node"]
# Wed, 16 Nov 2022 01:11:05 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Nov 2022 01:11:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Nov 2022 01:11:30 GMT
ENV NODE_ENV=production
# Wed, 16 Nov 2022 01:11:31 GMT
ENV GHOST_CLI_VERSION=1.23.1
# Wed, 16 Nov 2022 01:12:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 16 Nov 2022 01:12:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 16 Nov 2022 01:12:12 GMT
ENV GHOST_VERSION=5.22.10
# Wed, 16 Nov 2022 01:20:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 16 Nov 2022 01:21:15 GMT
WORKDIR /var/lib/ghost
# Wed, 16 Nov 2022 01:21:15 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 16 Nov 2022 01:21:16 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Wed, 16 Nov 2022 01:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 01:21:17 GMT
EXPOSE 2368
# Wed, 16 Nov 2022 01:21:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec8cf43615bdc08d7caf99cd83f8b51bc8716de831eda4a2f734b301c6a140`  
		Last Modified: Tue, 15 Nov 2022 08:19:59 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fda3a1e3ada00d249bc778488a797425cf7cd8050e77843ebeb0f5ea62f224`  
		Last Modified: Tue, 15 Nov 2022 08:22:25 GMT  
		Size: 35.4 MB (35370246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d9e5094e9573f77781bb698c378fad5e70b19e7980e000ecbfe5bbf2e5a500`  
		Last Modified: Tue, 15 Nov 2022 08:22:20 GMT  
		Size: 2.8 MB (2765674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553feeb25b7cd32c8934573fc885496b40e5ff89cf4bef4aae6d587b6d10cb2`  
		Last Modified: Tue, 15 Nov 2022 08:22:19 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8623d720f3c42dbe1854a0f481b08794fc213ed352d16b8208c1e0bc75e8fb`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 1.4 MB (1436312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c0510e8a3cd0f1b7a3ce052b46d206d04bad03bce28a3d60ed79d02f2b0c57`  
		Last Modified: Wed, 16 Nov 2022 01:36:29 GMT  
		Size: 10.2 MB (10225396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3596217afd671d877e64627a6697d89fcd62931b8ecad3beccd820614a3d2cf5`  
		Last Modified: Wed, 16 Nov 2022 01:36:42 GMT  
		Size: 78.1 MB (78106018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabdd107e4fb17c5e0b38ff8aee93fa48afa5019343da9a5f945332195fa946`  
		Last Modified: Wed, 16 Nov 2022 01:36:26 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

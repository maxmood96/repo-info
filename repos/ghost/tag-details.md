<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:4`](#ghost4)
-	[`ghost:4-alpine`](#ghost4-alpine)
-	[`ghost:4.44`](#ghost444)
-	[`ghost:4.44-alpine`](#ghost444-alpine)
-	[`ghost:4.44.0`](#ghost4440)
-	[`ghost:4.44.0-alpine`](#ghost4440-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:4`

```console
$ docker pull ghost@sha256:29ae24acabf010c1c4b41f5150f3b452cbcbaa13d6b4fdd84acdc41a7c860751
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
$ docker pull ghost@sha256:dcf72234dc1303677c14bcd1209024f694d24fbf0ed26f865adad6f40d65083c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151543699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cb5dc64a580976014b49b40719a817b63b1ff999fa1fecd6d7a0fb47e10dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:13:21 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 10:21:17 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 10:21:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 10:21:43 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 10:21:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 10:21:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:21:56 GMT
CMD ["node"]
# Thu, 21 Apr 2022 00:11:23 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 00:11:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 00:11:34 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:21:50 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:22:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:25:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:25:25 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:25:25 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:25:25 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 22:25:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:25:25 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:25:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e668081a27339473567eb3eafa1abbd3f5ceefaa67434d1748f8c46d4fdf6f93`  
		Last Modified: Wed, 20 Apr 2022 10:32:04 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d444f00d53b845fef8ee473fc7552d50c5e3e57fbb827950c268765b74fac00`  
		Last Modified: Wed, 20 Apr 2022 10:38:09 GMT  
		Size: 36.0 MB (36048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128a733a96c68606bdf399393f948360adf06c8f764dfdd018ee97787766a580`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 2.8 MB (2782020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e41e9aed24621d2afef40857683cc73a4c4b7f8edafca46393adfde99b2c35`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392af486ff5dbf6170c741891fcebec191cdf0e3c4c259066c793deecd9228d4`  
		Last Modified: Thu, 21 Apr 2022 00:15:29 GMT  
		Size: 1.4 MB (1448178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dceceeb7a32edbf92b0b1774e7c4d8bb5ee7359f152a487336d67d85900f4c8`  
		Last Modified: Thu, 21 Apr 2022 22:29:19 GMT  
		Size: 9.6 MB (9570265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2a24e4ad5d7372fccff886ddb62200a79ccd62b5109fa5fb86b47c1f5da943`  
		Last Modified: Thu, 21 Apr 2022 22:29:29 GMT  
		Size: 70.3 MB (70310984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a61eda0deea4d1392171921a14042695e0ac43122821b03710136c13d48033`  
		Last Modified: Thu, 21 Apr 2022 22:29:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fb63c0d5977b9249d7ab172fd66793968563a6dd7eb9139e1e9ce4367d473b61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154080429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e8fc193382395aeabfb43b785fb9872ab4df1f5cac0753233174175ad00c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 00:10:51 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 00:33:11 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 00:34:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 00:34:02 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 00:34:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 00:34:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 00:34:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 00:34:37 GMT
CMD ["node"]
# Fri, 22 Apr 2022 12:42:04 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 12:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 12:42:33 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:42:34 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:43:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:43:25 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:51:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:51:06 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:51:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:51:06 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 12:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:51:07 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:51:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34257bda5d3bc8816a1eb85fb98c52dbadc165802b744fe00e5faddf24f991f`  
		Last Modified: Thu, 21 Apr 2022 01:06:29 GMT  
		Size: 4.2 KB (4175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf55f73d31fce34821ae83bc50b171467d8a58cf9b933beb5934e7d980a8ed`  
		Last Modified: Thu, 21 Apr 2022 01:21:53 GMT  
		Size: 34.2 MB (34206825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd1b29f94636265d9da4c4e338481c420646410fc05c9deb7e5249e35e87e29`  
		Last Modified: Thu, 21 Apr 2022 01:21:31 GMT  
		Size: 2.8 MB (2772510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07331afdbc0a6a01673214e15f644bcea3f093d9eff5f6b229704c0ea423bb94`  
		Last Modified: Thu, 21 Apr 2022 01:21:29 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e1e05156a40d5bce75161ae5f726cf145e05bc9c8fbf34f8c28c1bd183ddc`  
		Last Modified: Fri, 22 Apr 2022 13:00:12 GMT  
		Size: 1.4 MB (1400368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5d91eea624399af581a48ea55e625d0c7cecbdaba19a9dc4e425ea18f826e7`  
		Last Modified: Fri, 22 Apr 2022 13:00:26 GMT  
		Size: 9.6 MB (9570576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeabdf632b0c643c388782fa3e87b2008897f032edabb392eeb5ac9f741ec54`  
		Last Modified: Fri, 22 Apr 2022 13:01:25 GMT  
		Size: 79.5 MB (79549224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c9f209a2361c029ddd688a21a6c7fd3e5a7bcf952ead5b3eb23a7ab14fc491`  
		Last Modified: Fri, 22 Apr 2022 13:00:11 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9aa8f6209d3c3009663bf6a8aee37577343eb3261e5c1d567a4e3d1cb6ec5e9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161658595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3122dbf6a0293d6db766fe1bfbc1faae9e712cfffd1a9d3291342650203ec789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:46:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 09:56:24 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 09:56:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 09:56:49 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 09:57:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 09:57:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 09:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 09:57:04 GMT
CMD ["node"]
# Thu, 21 Apr 2022 02:54:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 02:54:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 02:54:50 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:00:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:00:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:00:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:00:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:00:50 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:03:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:04:00 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:04:02 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:04:05 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 23:04:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:04:10 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:04:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcf03983304e3396f5948d3c624e30b772d1ff3509c706caed83ef28438f1da`  
		Last Modified: Wed, 20 Apr 2022 10:11:56 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4805c92d5c569c2f4495e0fd8e12a465f61fc0f5d5f4d89cc220b13ff2557411`  
		Last Modified: Wed, 20 Apr 2022 10:18:24 GMT  
		Size: 36.2 MB (36154398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6f866fefa758cc4823ad299004cbd908ed1c0d073b1004bf0b72f215c84828`  
		Last Modified: Wed, 20 Apr 2022 10:18:18 GMT  
		Size: 2.8 MB (2781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19f3a7274e477fc771ea00030f1c865c9a10c3e38e7aeb6be2d8a08599a25a`  
		Last Modified: Wed, 20 Apr 2022 10:18:17 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e79b5da82b9c170dd4b8cf196aab0fcc967a59ecf812e15dd5449b29d177fa9`  
		Last Modified: Thu, 21 Apr 2022 02:59:29 GMT  
		Size: 1.4 MB (1383713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2d9987c1e1828a89a66e4e776001ab45a14c9d3ac25ab5934cf0ee39ae70e`  
		Last Modified: Thu, 21 Apr 2022 23:09:08 GMT  
		Size: 9.6 MB (9570279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ca43bc7c56fb596b5bb021ee79aab4a7727b286c905cc83755dafbf56ba72`  
		Last Modified: Thu, 21 Apr 2022 23:09:20 GMT  
		Size: 81.7 MB (81697963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55adc76500a79cce32120afe64e6738e37cbd42204e03d7984ffa7733348869e`  
		Last Modified: Thu, 21 Apr 2022 23:09:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; ppc64le

```console
$ docker pull ghost@sha256:97cd1d65c37e5ff12351986abeadc8410445d54ebef0b20c8f5c850e9014d324
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153267439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b1656c8d38697ccc81c85e5452a5a77ab3df2cbb71e1480c559ab69bfd7ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 10:01:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 10:39:12 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 10:40:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 10:40:46 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 10:42:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 10:42:15 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 10:42:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 10:42:19 GMT
CMD ["node"]
# Fri, 22 Apr 2022 06:04:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 06:06:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 06:06:18 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 06:06:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 06:07:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 06:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 06:07:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 06:07:43 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 06:30:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 06:30:27 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 06:30:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 06:30:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 06:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 06:30:39 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 06:30:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dfd14f4b8dc5b2ece2300878fcb7f82a6c028640285e84df9d6b867d304b4`  
		Last Modified: Thu, 21 Apr 2022 12:45:37 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143b653e4afbc934d43808504513179596c43bcec6c5829b90aefa2a1655141c`  
		Last Modified: Thu, 21 Apr 2022 12:53:08 GMT  
		Size: 38.0 MB (37978299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7cab81867ac00e75a2224d1e0490e517d64a3c4722aa5cff6362296128f7e`  
		Last Modified: Thu, 21 Apr 2022 12:53:01 GMT  
		Size: 2.8 MB (2782412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3d94cf42096de509ac7f5188746e392eddc10a896233407fba98c7562dc9b`  
		Last Modified: Thu, 21 Apr 2022 12:53:00 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816ff917e2908244ff376fc99bc2f36f217a87ed39e8a423e1760a39acc4d973`  
		Last Modified: Fri, 22 Apr 2022 06:31:05 GMT  
		Size: 1.4 MB (1367679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7e8e32f1a52d3e639bccec6487d07e284dcc10a329b69899c14f54e4dfec7`  
		Last Modified: Fri, 22 Apr 2022 06:31:08 GMT  
		Size: 9.6 MB (9570563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54015f599eadbda12c0d070716b0be17e84831d918e0f530c7cd7f777fb40e0b`  
		Last Modified: Fri, 22 Apr 2022 06:31:22 GMT  
		Size: 66.3 MB (66278049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b08801e1ffbcd8cd4bad9689d2bd560716bb5a6da42590ccf4f83289b618ff`  
		Last Modified: Fri, 22 Apr 2022 06:31:04 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; s390x

```console
$ docker pull ghost@sha256:7dae1128c62949f7a1f6737c76f4cbaa620dd9ddda262aae0877989c670725eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145197955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df5b85a7a7075af8411748f327feca767a8d03287b304696c6179683f60a711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 13:03:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 13:10:46 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 13:11:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 13:11:13 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 13:11:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 13:11:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 13:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 13:11:24 GMT
CMD ["node"]
# Thu, 21 Apr 2022 07:15:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 07:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 07:15:37 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 00:03:55 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 00:05:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 00:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 00:21:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 00:22:08 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 00:22:08 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 00:22:09 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 00:22:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 00:22:09 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 00:22:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba080336cdb91a025d29d9b1a959402f181ed47358c5aabfe2baa9fbbdb2526`  
		Last Modified: Wed, 20 Apr 2022 13:21:37 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925bee1f31b092e56dc94873158d55cb00cd86545b7aac56ef6a494a1914dc16`  
		Last Modified: Wed, 20 Apr 2022 13:25:04 GMT  
		Size: 35.9 MB (35913825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100515451ae271e479c404cf7ad8b5bd8ac5b200fb51b3549c392338843d51c4`  
		Last Modified: Wed, 20 Apr 2022 13:25:00 GMT  
		Size: 2.8 MB (2783085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33294f3eb8fb473f81134c1152e757722051c32cd70ab61f26397f548d16d9ad`  
		Last Modified: Wed, 20 Apr 2022 13:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0219c13a23e2876d5d7e61f468c0af6df28544c16e3b91297ceabd2e0d4f7`  
		Last Modified: Thu, 21 Apr 2022 07:19:46 GMT  
		Size: 1.4 MB (1435082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edb84d1f4bcc5228531be258c5e5fb559211e773ea04528ef9646faea2f3f9`  
		Last Modified: Fri, 22 Apr 2022 00:22:41 GMT  
		Size: 9.6 MB (9570616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b0ae9fc8a5c17363e53126553ef9e33748dbc990389ee3b0d1e7975ef7717`  
		Last Modified: Fri, 22 Apr 2022 00:22:50 GMT  
		Size: 65.8 MB (65835359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28594230d81842fb65dd01ee7dcfda86421a415f56510caf408464cd231c23`  
		Last Modified: Fri, 22 Apr 2022 00:22:39 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4-alpine`

```console
$ docker pull ghost@sha256:09157352e9ea076529679e7d31b13bd6569408731f93945a3cf9f05600453e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:df796a02fd7cf35870d8d28d2956f3b7eee84d108f346c4f072bac87699e0cad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123093602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2a36dee5865a44db3568de3ec4073800e9d55d4529cc42419fbadcc962a93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:11:16 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 10:11:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 10:11:25 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 10:11:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 10:11:30 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:11:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 10:11:30 GMT
CMD ["node"]
# Tue, 05 Apr 2022 15:54:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 15:54:31 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 15:54:31 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:25:28 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:25:51 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:25:51 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:28:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:28:52 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:28:52 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:28:52 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 22:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:28:52 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:28:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f77dc7475a9ee1adc8d2d5488f32f32738586bd2d990b8e1caa80544a30572`  
		Last Modified: Tue, 05 Apr 2022 10:18:09 GMT  
		Size: 37.1 MB (37132761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0229f3f8988db17639cba0c34bf5b284794200e08a64b2e7e8d1e2a951a42dbf`  
		Last Modified: Tue, 05 Apr 2022 10:18:04 GMT  
		Size: 2.4 MB (2358380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ba6c2a71cc186b7d902e57a76b3ab2839273e293f35edf69dfc28a4e7fc864`  
		Last Modified: Tue, 05 Apr 2022 10:18:03 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ce844d16ce9093f01a858beb09d6ea6b265045575d2e17a8332bd5a24cc16`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac48c6254796bcd50706c0855803821724adfb9870c4a5e81aaf7d85b86ddfb0`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 817.2 KB (817176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af283bf213bc2ff10d2387b35dcf2e46b595ef162af50d0ee6f82f712108c5f`  
		Last Modified: Thu, 21 Apr 2022 22:29:47 GMT  
		Size: 9.6 MB (9570321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfed21aca3ad21d702b547fc250ebf1e5fa1d7d24b350a445e01d089b0d2c98`  
		Last Modified: Thu, 21 Apr 2022 22:29:57 GMT  
		Size: 70.4 MB (70384385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ebcadede294e08bf68ebdeb776b89260dbe3bbaadc5cb24720ac86a198e72`  
		Last Modified: Thu, 21 Apr 2022 22:29:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:230bec2aef8fa0cd397c4f7f5c9709761bdc598d8509dac6700fbb9909e73beb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115333582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56781ad6b302e62f470137103ccf7f07728f8274d842347fe0518104e3fa49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:26:29 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 05:40:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 05:40:06 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 05:40:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 05:40:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 05:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 05:40:15 GMT
CMD ["node"]
# Tue, 05 Apr 2022 18:24:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 18:24:40 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 18:24:40 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:49:35 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:50:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:50:51 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:00:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:00:10 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:00:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:00:11 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:00:12 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:00:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3354dc99866b12a88c4bd7ed711488887cbed01d841e9794c65e7592cead0e42`  
		Last Modified: Tue, 05 Apr 2022 06:36:00 GMT  
		Size: 36.2 MB (36198138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1a58fa44a08ad15f35491309df29537157889803b60be33bdcb0664e2a587f`  
		Last Modified: Tue, 05 Apr 2022 06:35:36 GMT  
		Size: 2.4 MB (2418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d8ebe696986f6652a7ed3c86ac8ba3793d5119d8afd3b128a1e9a18cb70c1`  
		Last Modified: Tue, 05 Apr 2022 06:35:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61091aa7bda313caca280046e5231603b20ac0bf519ec7c8660178bd8c2f9d44`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 11.0 KB (10974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633c6d790ae1e67a13d13aca30e70be2f0eae095032a15f16a6c85414b0f669`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 771.2 KB (771175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ff3529d9e58c2564925c042f63c2955a6cc649aea978bf0933966ee357b55a`  
		Last Modified: Thu, 21 Apr 2022 23:01:07 GMT  
		Size: 9.6 MB (9570632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08f662c1d4c2beef8d944f6bab58a6b3ebb1f758e824e540c4d243a1107f68`  
		Last Modified: Thu, 21 Apr 2022 23:01:48 GMT  
		Size: 63.7 MB (63737150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba68ac064a5e907fdebb93f13a85c4ce6553bbf26724b085d4fb39924965fad`  
		Last Modified: Thu, 21 Apr 2022 23:00:52 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b726c091588289db1bbdea4ac9cd4a1fedcfd37fb93280fbfd124113fd86a4d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114164496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee1d6d1cc42b5a325acdb33dcd4c3ce5c5bb2f83335ed46f7533fca22cbe3e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 17:43:03 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 17:55:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 17:55:54 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 17:56:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 17:56:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 17:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 17:56:03 GMT
CMD ["node"]
# Wed, 06 Apr 2022 02:45:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 06 Apr 2022 02:45:39 GMT
RUN apk add --no-cache 		bash
# Wed, 06 Apr 2022 02:45:39 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:51:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:52:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:52:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:59:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:59:17 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:59:18 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:59:18 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Apr 2022 12:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:59:19 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:59:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3df1e2806696dbaefd6243268e71b96d0bcc55e4e0200bb608e50e9472b720`  
		Last Modified: Tue, 05 Apr 2022 19:02:58 GMT  
		Size: 35.8 MB (35751067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09205dfcd8b25ca660d2dfd77d64e8e49af76687cccba75fbb7f876e77c393b0`  
		Last Modified: Tue, 05 Apr 2022 19:02:36 GMT  
		Size: 2.4 MB (2418454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e036f8d684cce25c16a09e061c8bff2abdbea00d775921960e82a7522cef2`  
		Last Modified: Tue, 05 Apr 2022 19:02:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251af54f86884a25fdd443f42b9a4b98657feca7ec58c23906c88699d006b556`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 10.8 KB (10770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46253eacab6b15a2fa733739521d11aa8347847dfd13258a776db2356f6c44`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 704.1 KB (704134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1df2bbc6958308178c27d7394faecd48ebc5d931de77dc4fc206693140028`  
		Last Modified: Fri, 22 Apr 2022 13:02:01 GMT  
		Size: 9.6 MB (9570602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1d6a69a41962a4b57a309945b871f09d7221da8e489b20fff26326ba745a38`  
		Last Modified: Fri, 22 Apr 2022 13:02:52 GMT  
		Size: 63.3 MB (63280500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5a8e6f14e8f948f86787b1b667c57bcac324f97cb8b4895c99d7f4e8b71e7`  
		Last Modified: Fri, 22 Apr 2022 13:01:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e080be80d222d9f3a99a535ca1f8919e481805fd00cf8217be64e32ec214b746
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133741681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7423f42d5f279e76f5ccb7054acc2d966aa76b459b8421d57b7040f1351d7367`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:10:00 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 11:29:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 11:29:56 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 11:30:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 11:30:04 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:30:05 GMT
CMD ["node"]
# Tue, 05 Apr 2022 17:40:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 17:40:56 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 17:40:57 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:04:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:04:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:04:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:04:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:04:48 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:08:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:08:29 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:08:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:08:34 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:08:39 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:08:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10981ae1a586f08fc64f5e03af14d53d489f3d7762b11a35f4e0e650a871f3b`  
		Last Modified: Tue, 05 Apr 2022 14:16:18 GMT  
		Size: 37.0 MB (37013669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379155faf1aa767ddbc2287fb89a7a8dcead27019d96b6b2046649ee936df951`  
		Last Modified: Tue, 05 Apr 2022 14:16:12 GMT  
		Size: 2.4 MB (2425558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c4fa407cbf0ddea9951284ad9e593b19f9158ee60f6ae61868b179698a75cd`  
		Last Modified: Tue, 05 Apr 2022 14:16:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f79cb613167b8dc819ee3651e614a3b07f5182f73fd37f990f92075b6dfc7f`  
		Last Modified: Tue, 05 Apr 2022 17:45:58 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea380f558fd6b4eecfa37b880e2d489e98e7ebe10d366ef0004f1ef3f3b16ce`  
		Last Modified: Tue, 05 Apr 2022 17:45:59 GMT  
		Size: 826.3 KB (826295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcffbbf76d14f11471479d15f5b7eed819189fd961749b0be7134aa472a3922b`  
		Last Modified: Thu, 21 Apr 2022 23:09:40 GMT  
		Size: 9.6 MB (9570230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2717e5cf0c28b9bb7dca8e07c7ccf5cd52aa4f0f381b0ca1742001ca47f028`  
		Last Modified: Thu, 21 Apr 2022 23:09:52 GMT  
		Size: 81.2 MB (81176546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8239852696e954fa3520fb4475ef4715eaadb69d9abf4ace59f267953fb4bb30`  
		Last Modified: Thu, 21 Apr 2022 23:09:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.44`

```console
$ docker pull ghost@sha256:29ae24acabf010c1c4b41f5150f3b452cbcbaa13d6b4fdd84acdc41a7c860751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.44` - linux; amd64

```console
$ docker pull ghost@sha256:dcf72234dc1303677c14bcd1209024f694d24fbf0ed26f865adad6f40d65083c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151543699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cb5dc64a580976014b49b40719a817b63b1ff999fa1fecd6d7a0fb47e10dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:13:21 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 10:21:17 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 10:21:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 10:21:43 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 10:21:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 10:21:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:21:56 GMT
CMD ["node"]
# Thu, 21 Apr 2022 00:11:23 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 00:11:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 00:11:34 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:21:50 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:22:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:25:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:25:25 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:25:25 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:25:25 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 22:25:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:25:25 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:25:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e668081a27339473567eb3eafa1abbd3f5ceefaa67434d1748f8c46d4fdf6f93`  
		Last Modified: Wed, 20 Apr 2022 10:32:04 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d444f00d53b845fef8ee473fc7552d50c5e3e57fbb827950c268765b74fac00`  
		Last Modified: Wed, 20 Apr 2022 10:38:09 GMT  
		Size: 36.0 MB (36048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128a733a96c68606bdf399393f948360adf06c8f764dfdd018ee97787766a580`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 2.8 MB (2782020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e41e9aed24621d2afef40857683cc73a4c4b7f8edafca46393adfde99b2c35`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392af486ff5dbf6170c741891fcebec191cdf0e3c4c259066c793deecd9228d4`  
		Last Modified: Thu, 21 Apr 2022 00:15:29 GMT  
		Size: 1.4 MB (1448178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dceceeb7a32edbf92b0b1774e7c4d8bb5ee7359f152a487336d67d85900f4c8`  
		Last Modified: Thu, 21 Apr 2022 22:29:19 GMT  
		Size: 9.6 MB (9570265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2a24e4ad5d7372fccff886ddb62200a79ccd62b5109fa5fb86b47c1f5da943`  
		Last Modified: Thu, 21 Apr 2022 22:29:29 GMT  
		Size: 70.3 MB (70310984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a61eda0deea4d1392171921a14042695e0ac43122821b03710136c13d48033`  
		Last Modified: Thu, 21 Apr 2022 22:29:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fb63c0d5977b9249d7ab172fd66793968563a6dd7eb9139e1e9ce4367d473b61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154080429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e8fc193382395aeabfb43b785fb9872ab4df1f5cac0753233174175ad00c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 00:10:51 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 00:33:11 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 00:34:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 00:34:02 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 00:34:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 00:34:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 00:34:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 00:34:37 GMT
CMD ["node"]
# Fri, 22 Apr 2022 12:42:04 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 12:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 12:42:33 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:42:34 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:43:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:43:25 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:51:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:51:06 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:51:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:51:06 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 12:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:51:07 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:51:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34257bda5d3bc8816a1eb85fb98c52dbadc165802b744fe00e5faddf24f991f`  
		Last Modified: Thu, 21 Apr 2022 01:06:29 GMT  
		Size: 4.2 KB (4175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf55f73d31fce34821ae83bc50b171467d8a58cf9b933beb5934e7d980a8ed`  
		Last Modified: Thu, 21 Apr 2022 01:21:53 GMT  
		Size: 34.2 MB (34206825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd1b29f94636265d9da4c4e338481c420646410fc05c9deb7e5249e35e87e29`  
		Last Modified: Thu, 21 Apr 2022 01:21:31 GMT  
		Size: 2.8 MB (2772510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07331afdbc0a6a01673214e15f644bcea3f093d9eff5f6b229704c0ea423bb94`  
		Last Modified: Thu, 21 Apr 2022 01:21:29 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e1e05156a40d5bce75161ae5f726cf145e05bc9c8fbf34f8c28c1bd183ddc`  
		Last Modified: Fri, 22 Apr 2022 13:00:12 GMT  
		Size: 1.4 MB (1400368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5d91eea624399af581a48ea55e625d0c7cecbdaba19a9dc4e425ea18f826e7`  
		Last Modified: Fri, 22 Apr 2022 13:00:26 GMT  
		Size: 9.6 MB (9570576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeabdf632b0c643c388782fa3e87b2008897f032edabb392eeb5ac9f741ec54`  
		Last Modified: Fri, 22 Apr 2022 13:01:25 GMT  
		Size: 79.5 MB (79549224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c9f209a2361c029ddd688a21a6c7fd3e5a7bcf952ead5b3eb23a7ab14fc491`  
		Last Modified: Fri, 22 Apr 2022 13:00:11 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9aa8f6209d3c3009663bf6a8aee37577343eb3261e5c1d567a4e3d1cb6ec5e9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161658595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3122dbf6a0293d6db766fe1bfbc1faae9e712cfffd1a9d3291342650203ec789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:46:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 09:56:24 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 09:56:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 09:56:49 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 09:57:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 09:57:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 09:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 09:57:04 GMT
CMD ["node"]
# Thu, 21 Apr 2022 02:54:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 02:54:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 02:54:50 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:00:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:00:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:00:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:00:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:00:50 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:03:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:04:00 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:04:02 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:04:05 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 23:04:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:04:10 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:04:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcf03983304e3396f5948d3c624e30b772d1ff3509c706caed83ef28438f1da`  
		Last Modified: Wed, 20 Apr 2022 10:11:56 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4805c92d5c569c2f4495e0fd8e12a465f61fc0f5d5f4d89cc220b13ff2557411`  
		Last Modified: Wed, 20 Apr 2022 10:18:24 GMT  
		Size: 36.2 MB (36154398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6f866fefa758cc4823ad299004cbd908ed1c0d073b1004bf0b72f215c84828`  
		Last Modified: Wed, 20 Apr 2022 10:18:18 GMT  
		Size: 2.8 MB (2781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19f3a7274e477fc771ea00030f1c865c9a10c3e38e7aeb6be2d8a08599a25a`  
		Last Modified: Wed, 20 Apr 2022 10:18:17 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e79b5da82b9c170dd4b8cf196aab0fcc967a59ecf812e15dd5449b29d177fa9`  
		Last Modified: Thu, 21 Apr 2022 02:59:29 GMT  
		Size: 1.4 MB (1383713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2d9987c1e1828a89a66e4e776001ab45a14c9d3ac25ab5934cf0ee39ae70e`  
		Last Modified: Thu, 21 Apr 2022 23:09:08 GMT  
		Size: 9.6 MB (9570279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ca43bc7c56fb596b5bb021ee79aab4a7727b286c905cc83755dafbf56ba72`  
		Last Modified: Thu, 21 Apr 2022 23:09:20 GMT  
		Size: 81.7 MB (81697963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55adc76500a79cce32120afe64e6738e37cbd42204e03d7984ffa7733348869e`  
		Last Modified: Thu, 21 Apr 2022 23:09:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44` - linux; ppc64le

```console
$ docker pull ghost@sha256:97cd1d65c37e5ff12351986abeadc8410445d54ebef0b20c8f5c850e9014d324
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153267439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b1656c8d38697ccc81c85e5452a5a77ab3df2cbb71e1480c559ab69bfd7ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 10:01:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 10:39:12 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 10:40:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 10:40:46 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 10:42:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 10:42:15 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 10:42:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 10:42:19 GMT
CMD ["node"]
# Fri, 22 Apr 2022 06:04:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 06:06:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 06:06:18 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 06:06:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 06:07:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 06:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 06:07:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 06:07:43 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 06:30:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 06:30:27 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 06:30:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 06:30:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 06:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 06:30:39 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 06:30:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dfd14f4b8dc5b2ece2300878fcb7f82a6c028640285e84df9d6b867d304b4`  
		Last Modified: Thu, 21 Apr 2022 12:45:37 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143b653e4afbc934d43808504513179596c43bcec6c5829b90aefa2a1655141c`  
		Last Modified: Thu, 21 Apr 2022 12:53:08 GMT  
		Size: 38.0 MB (37978299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7cab81867ac00e75a2224d1e0490e517d64a3c4722aa5cff6362296128f7e`  
		Last Modified: Thu, 21 Apr 2022 12:53:01 GMT  
		Size: 2.8 MB (2782412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3d94cf42096de509ac7f5188746e392eddc10a896233407fba98c7562dc9b`  
		Last Modified: Thu, 21 Apr 2022 12:53:00 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816ff917e2908244ff376fc99bc2f36f217a87ed39e8a423e1760a39acc4d973`  
		Last Modified: Fri, 22 Apr 2022 06:31:05 GMT  
		Size: 1.4 MB (1367679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7e8e32f1a52d3e639bccec6487d07e284dcc10a329b69899c14f54e4dfec7`  
		Last Modified: Fri, 22 Apr 2022 06:31:08 GMT  
		Size: 9.6 MB (9570563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54015f599eadbda12c0d070716b0be17e84831d918e0f530c7cd7f777fb40e0b`  
		Last Modified: Fri, 22 Apr 2022 06:31:22 GMT  
		Size: 66.3 MB (66278049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b08801e1ffbcd8cd4bad9689d2bd560716bb5a6da42590ccf4f83289b618ff`  
		Last Modified: Fri, 22 Apr 2022 06:31:04 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44` - linux; s390x

```console
$ docker pull ghost@sha256:7dae1128c62949f7a1f6737c76f4cbaa620dd9ddda262aae0877989c670725eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145197955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df5b85a7a7075af8411748f327feca767a8d03287b304696c6179683f60a711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 13:03:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 13:10:46 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 13:11:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 13:11:13 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 13:11:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 13:11:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 13:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 13:11:24 GMT
CMD ["node"]
# Thu, 21 Apr 2022 07:15:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 07:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 07:15:37 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 00:03:55 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 00:05:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 00:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 00:21:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 00:22:08 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 00:22:08 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 00:22:09 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 00:22:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 00:22:09 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 00:22:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba080336cdb91a025d29d9b1a959402f181ed47358c5aabfe2baa9fbbdb2526`  
		Last Modified: Wed, 20 Apr 2022 13:21:37 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925bee1f31b092e56dc94873158d55cb00cd86545b7aac56ef6a494a1914dc16`  
		Last Modified: Wed, 20 Apr 2022 13:25:04 GMT  
		Size: 35.9 MB (35913825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100515451ae271e479c404cf7ad8b5bd8ac5b200fb51b3549c392338843d51c4`  
		Last Modified: Wed, 20 Apr 2022 13:25:00 GMT  
		Size: 2.8 MB (2783085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33294f3eb8fb473f81134c1152e757722051c32cd70ab61f26397f548d16d9ad`  
		Last Modified: Wed, 20 Apr 2022 13:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0219c13a23e2876d5d7e61f468c0af6df28544c16e3b91297ceabd2e0d4f7`  
		Last Modified: Thu, 21 Apr 2022 07:19:46 GMT  
		Size: 1.4 MB (1435082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edb84d1f4bcc5228531be258c5e5fb559211e773ea04528ef9646faea2f3f9`  
		Last Modified: Fri, 22 Apr 2022 00:22:41 GMT  
		Size: 9.6 MB (9570616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b0ae9fc8a5c17363e53126553ef9e33748dbc990389ee3b0d1e7975ef7717`  
		Last Modified: Fri, 22 Apr 2022 00:22:50 GMT  
		Size: 65.8 MB (65835359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28594230d81842fb65dd01ee7dcfda86421a415f56510caf408464cd231c23`  
		Last Modified: Fri, 22 Apr 2022 00:22:39 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.44-alpine`

```console
$ docker pull ghost@sha256:09157352e9ea076529679e7d31b13bd6569408731f93945a3cf9f05600453e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4.44-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:df796a02fd7cf35870d8d28d2956f3b7eee84d108f346c4f072bac87699e0cad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123093602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2a36dee5865a44db3568de3ec4073800e9d55d4529cc42419fbadcc962a93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:11:16 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 10:11:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 10:11:25 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 10:11:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 10:11:30 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:11:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 10:11:30 GMT
CMD ["node"]
# Tue, 05 Apr 2022 15:54:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 15:54:31 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 15:54:31 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:25:28 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:25:51 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:25:51 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:28:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:28:52 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:28:52 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:28:52 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 22:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:28:52 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:28:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f77dc7475a9ee1adc8d2d5488f32f32738586bd2d990b8e1caa80544a30572`  
		Last Modified: Tue, 05 Apr 2022 10:18:09 GMT  
		Size: 37.1 MB (37132761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0229f3f8988db17639cba0c34bf5b284794200e08a64b2e7e8d1e2a951a42dbf`  
		Last Modified: Tue, 05 Apr 2022 10:18:04 GMT  
		Size: 2.4 MB (2358380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ba6c2a71cc186b7d902e57a76b3ab2839273e293f35edf69dfc28a4e7fc864`  
		Last Modified: Tue, 05 Apr 2022 10:18:03 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ce844d16ce9093f01a858beb09d6ea6b265045575d2e17a8332bd5a24cc16`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac48c6254796bcd50706c0855803821724adfb9870c4a5e81aaf7d85b86ddfb0`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 817.2 KB (817176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af283bf213bc2ff10d2387b35dcf2e46b595ef162af50d0ee6f82f712108c5f`  
		Last Modified: Thu, 21 Apr 2022 22:29:47 GMT  
		Size: 9.6 MB (9570321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfed21aca3ad21d702b547fc250ebf1e5fa1d7d24b350a445e01d089b0d2c98`  
		Last Modified: Thu, 21 Apr 2022 22:29:57 GMT  
		Size: 70.4 MB (70384385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ebcadede294e08bf68ebdeb776b89260dbe3bbaadc5cb24720ac86a198e72`  
		Last Modified: Thu, 21 Apr 2022 22:29:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:230bec2aef8fa0cd397c4f7f5c9709761bdc598d8509dac6700fbb9909e73beb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115333582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56781ad6b302e62f470137103ccf7f07728f8274d842347fe0518104e3fa49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:26:29 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 05:40:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 05:40:06 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 05:40:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 05:40:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 05:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 05:40:15 GMT
CMD ["node"]
# Tue, 05 Apr 2022 18:24:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 18:24:40 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 18:24:40 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:49:35 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:50:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:50:51 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:00:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:00:10 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:00:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:00:11 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:00:12 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:00:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3354dc99866b12a88c4bd7ed711488887cbed01d841e9794c65e7592cead0e42`  
		Last Modified: Tue, 05 Apr 2022 06:36:00 GMT  
		Size: 36.2 MB (36198138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1a58fa44a08ad15f35491309df29537157889803b60be33bdcb0664e2a587f`  
		Last Modified: Tue, 05 Apr 2022 06:35:36 GMT  
		Size: 2.4 MB (2418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d8ebe696986f6652a7ed3c86ac8ba3793d5119d8afd3b128a1e9a18cb70c1`  
		Last Modified: Tue, 05 Apr 2022 06:35:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61091aa7bda313caca280046e5231603b20ac0bf519ec7c8660178bd8c2f9d44`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 11.0 KB (10974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633c6d790ae1e67a13d13aca30e70be2f0eae095032a15f16a6c85414b0f669`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 771.2 KB (771175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ff3529d9e58c2564925c042f63c2955a6cc649aea978bf0933966ee357b55a`  
		Last Modified: Thu, 21 Apr 2022 23:01:07 GMT  
		Size: 9.6 MB (9570632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08f662c1d4c2beef8d944f6bab58a6b3ebb1f758e824e540c4d243a1107f68`  
		Last Modified: Thu, 21 Apr 2022 23:01:48 GMT  
		Size: 63.7 MB (63737150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba68ac064a5e907fdebb93f13a85c4ce6553bbf26724b085d4fb39924965fad`  
		Last Modified: Thu, 21 Apr 2022 23:00:52 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b726c091588289db1bbdea4ac9cd4a1fedcfd37fb93280fbfd124113fd86a4d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114164496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee1d6d1cc42b5a325acdb33dcd4c3ce5c5bb2f83335ed46f7533fca22cbe3e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 17:43:03 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 17:55:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 17:55:54 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 17:56:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 17:56:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 17:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 17:56:03 GMT
CMD ["node"]
# Wed, 06 Apr 2022 02:45:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 06 Apr 2022 02:45:39 GMT
RUN apk add --no-cache 		bash
# Wed, 06 Apr 2022 02:45:39 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:51:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:52:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:52:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:59:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:59:17 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:59:18 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:59:18 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Apr 2022 12:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:59:19 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:59:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3df1e2806696dbaefd6243268e71b96d0bcc55e4e0200bb608e50e9472b720`  
		Last Modified: Tue, 05 Apr 2022 19:02:58 GMT  
		Size: 35.8 MB (35751067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09205dfcd8b25ca660d2dfd77d64e8e49af76687cccba75fbb7f876e77c393b0`  
		Last Modified: Tue, 05 Apr 2022 19:02:36 GMT  
		Size: 2.4 MB (2418454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e036f8d684cce25c16a09e061c8bff2abdbea00d775921960e82a7522cef2`  
		Last Modified: Tue, 05 Apr 2022 19:02:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251af54f86884a25fdd443f42b9a4b98657feca7ec58c23906c88699d006b556`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 10.8 KB (10770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46253eacab6b15a2fa733739521d11aa8347847dfd13258a776db2356f6c44`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 704.1 KB (704134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1df2bbc6958308178c27d7394faecd48ebc5d931de77dc4fc206693140028`  
		Last Modified: Fri, 22 Apr 2022 13:02:01 GMT  
		Size: 9.6 MB (9570602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1d6a69a41962a4b57a309945b871f09d7221da8e489b20fff26326ba745a38`  
		Last Modified: Fri, 22 Apr 2022 13:02:52 GMT  
		Size: 63.3 MB (63280500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5a8e6f14e8f948f86787b1b667c57bcac324f97cb8b4895c99d7f4e8b71e7`  
		Last Modified: Fri, 22 Apr 2022 13:01:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e080be80d222d9f3a99a535ca1f8919e481805fd00cf8217be64e32ec214b746
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133741681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7423f42d5f279e76f5ccb7054acc2d966aa76b459b8421d57b7040f1351d7367`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:10:00 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 11:29:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 11:29:56 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 11:30:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 11:30:04 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:30:05 GMT
CMD ["node"]
# Tue, 05 Apr 2022 17:40:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 17:40:56 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 17:40:57 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:04:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:04:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:04:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:04:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:04:48 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:08:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:08:29 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:08:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:08:34 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:08:39 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:08:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10981ae1a586f08fc64f5e03af14d53d489f3d7762b11a35f4e0e650a871f3b`  
		Last Modified: Tue, 05 Apr 2022 14:16:18 GMT  
		Size: 37.0 MB (37013669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379155faf1aa767ddbc2287fb89a7a8dcead27019d96b6b2046649ee936df951`  
		Last Modified: Tue, 05 Apr 2022 14:16:12 GMT  
		Size: 2.4 MB (2425558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c4fa407cbf0ddea9951284ad9e593b19f9158ee60f6ae61868b179698a75cd`  
		Last Modified: Tue, 05 Apr 2022 14:16:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f79cb613167b8dc819ee3651e614a3b07f5182f73fd37f990f92075b6dfc7f`  
		Last Modified: Tue, 05 Apr 2022 17:45:58 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea380f558fd6b4eecfa37b880e2d489e98e7ebe10d366ef0004f1ef3f3b16ce`  
		Last Modified: Tue, 05 Apr 2022 17:45:59 GMT  
		Size: 826.3 KB (826295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcffbbf76d14f11471479d15f5b7eed819189fd961749b0be7134aa472a3922b`  
		Last Modified: Thu, 21 Apr 2022 23:09:40 GMT  
		Size: 9.6 MB (9570230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2717e5cf0c28b9bb7dca8e07c7ccf5cd52aa4f0f381b0ca1742001ca47f028`  
		Last Modified: Thu, 21 Apr 2022 23:09:52 GMT  
		Size: 81.2 MB (81176546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8239852696e954fa3520fb4475ef4715eaadb69d9abf4ace59f267953fb4bb30`  
		Last Modified: Thu, 21 Apr 2022 23:09:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.44.0`

```console
$ docker pull ghost@sha256:29ae24acabf010c1c4b41f5150f3b452cbcbaa13d6b4fdd84acdc41a7c860751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.44.0` - linux; amd64

```console
$ docker pull ghost@sha256:dcf72234dc1303677c14bcd1209024f694d24fbf0ed26f865adad6f40d65083c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151543699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cb5dc64a580976014b49b40719a817b63b1ff999fa1fecd6d7a0fb47e10dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:13:21 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 10:21:17 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 10:21:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 10:21:43 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 10:21:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 10:21:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:21:56 GMT
CMD ["node"]
# Thu, 21 Apr 2022 00:11:23 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 00:11:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 00:11:34 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:21:50 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:22:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:25:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:25:25 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:25:25 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:25:25 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 22:25:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:25:25 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:25:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e668081a27339473567eb3eafa1abbd3f5ceefaa67434d1748f8c46d4fdf6f93`  
		Last Modified: Wed, 20 Apr 2022 10:32:04 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d444f00d53b845fef8ee473fc7552d50c5e3e57fbb827950c268765b74fac00`  
		Last Modified: Wed, 20 Apr 2022 10:38:09 GMT  
		Size: 36.0 MB (36048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128a733a96c68606bdf399393f948360adf06c8f764dfdd018ee97787766a580`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 2.8 MB (2782020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e41e9aed24621d2afef40857683cc73a4c4b7f8edafca46393adfde99b2c35`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392af486ff5dbf6170c741891fcebec191cdf0e3c4c259066c793deecd9228d4`  
		Last Modified: Thu, 21 Apr 2022 00:15:29 GMT  
		Size: 1.4 MB (1448178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dceceeb7a32edbf92b0b1774e7c4d8bb5ee7359f152a487336d67d85900f4c8`  
		Last Modified: Thu, 21 Apr 2022 22:29:19 GMT  
		Size: 9.6 MB (9570265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2a24e4ad5d7372fccff886ddb62200a79ccd62b5109fa5fb86b47c1f5da943`  
		Last Modified: Thu, 21 Apr 2022 22:29:29 GMT  
		Size: 70.3 MB (70310984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a61eda0deea4d1392171921a14042695e0ac43122821b03710136c13d48033`  
		Last Modified: Thu, 21 Apr 2022 22:29:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fb63c0d5977b9249d7ab172fd66793968563a6dd7eb9139e1e9ce4367d473b61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154080429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e8fc193382395aeabfb43b785fb9872ab4df1f5cac0753233174175ad00c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 00:10:51 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 00:33:11 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 00:34:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 00:34:02 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 00:34:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 00:34:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 00:34:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 00:34:37 GMT
CMD ["node"]
# Fri, 22 Apr 2022 12:42:04 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 12:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 12:42:33 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:42:34 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:43:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:43:25 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:51:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:51:06 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:51:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:51:06 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 12:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:51:07 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:51:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34257bda5d3bc8816a1eb85fb98c52dbadc165802b744fe00e5faddf24f991f`  
		Last Modified: Thu, 21 Apr 2022 01:06:29 GMT  
		Size: 4.2 KB (4175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf55f73d31fce34821ae83bc50b171467d8a58cf9b933beb5934e7d980a8ed`  
		Last Modified: Thu, 21 Apr 2022 01:21:53 GMT  
		Size: 34.2 MB (34206825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd1b29f94636265d9da4c4e338481c420646410fc05c9deb7e5249e35e87e29`  
		Last Modified: Thu, 21 Apr 2022 01:21:31 GMT  
		Size: 2.8 MB (2772510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07331afdbc0a6a01673214e15f644bcea3f093d9eff5f6b229704c0ea423bb94`  
		Last Modified: Thu, 21 Apr 2022 01:21:29 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e1e05156a40d5bce75161ae5f726cf145e05bc9c8fbf34f8c28c1bd183ddc`  
		Last Modified: Fri, 22 Apr 2022 13:00:12 GMT  
		Size: 1.4 MB (1400368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5d91eea624399af581a48ea55e625d0c7cecbdaba19a9dc4e425ea18f826e7`  
		Last Modified: Fri, 22 Apr 2022 13:00:26 GMT  
		Size: 9.6 MB (9570576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeabdf632b0c643c388782fa3e87b2008897f032edabb392eeb5ac9f741ec54`  
		Last Modified: Fri, 22 Apr 2022 13:01:25 GMT  
		Size: 79.5 MB (79549224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c9f209a2361c029ddd688a21a6c7fd3e5a7bcf952ead5b3eb23a7ab14fc491`  
		Last Modified: Fri, 22 Apr 2022 13:00:11 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9aa8f6209d3c3009663bf6a8aee37577343eb3261e5c1d567a4e3d1cb6ec5e9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161658595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3122dbf6a0293d6db766fe1bfbc1faae9e712cfffd1a9d3291342650203ec789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:46:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 09:56:24 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 09:56:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 09:56:49 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 09:57:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 09:57:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 09:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 09:57:04 GMT
CMD ["node"]
# Thu, 21 Apr 2022 02:54:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 02:54:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 02:54:50 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:00:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:00:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:00:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:00:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:00:50 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:03:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:04:00 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:04:02 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:04:05 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 23:04:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:04:10 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:04:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcf03983304e3396f5948d3c624e30b772d1ff3509c706caed83ef28438f1da`  
		Last Modified: Wed, 20 Apr 2022 10:11:56 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4805c92d5c569c2f4495e0fd8e12a465f61fc0f5d5f4d89cc220b13ff2557411`  
		Last Modified: Wed, 20 Apr 2022 10:18:24 GMT  
		Size: 36.2 MB (36154398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6f866fefa758cc4823ad299004cbd908ed1c0d073b1004bf0b72f215c84828`  
		Last Modified: Wed, 20 Apr 2022 10:18:18 GMT  
		Size: 2.8 MB (2781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19f3a7274e477fc771ea00030f1c865c9a10c3e38e7aeb6be2d8a08599a25a`  
		Last Modified: Wed, 20 Apr 2022 10:18:17 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e79b5da82b9c170dd4b8cf196aab0fcc967a59ecf812e15dd5449b29d177fa9`  
		Last Modified: Thu, 21 Apr 2022 02:59:29 GMT  
		Size: 1.4 MB (1383713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2d9987c1e1828a89a66e4e776001ab45a14c9d3ac25ab5934cf0ee39ae70e`  
		Last Modified: Thu, 21 Apr 2022 23:09:08 GMT  
		Size: 9.6 MB (9570279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ca43bc7c56fb596b5bb021ee79aab4a7727b286c905cc83755dafbf56ba72`  
		Last Modified: Thu, 21 Apr 2022 23:09:20 GMT  
		Size: 81.7 MB (81697963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55adc76500a79cce32120afe64e6738e37cbd42204e03d7984ffa7733348869e`  
		Last Modified: Thu, 21 Apr 2022 23:09:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:97cd1d65c37e5ff12351986abeadc8410445d54ebef0b20c8f5c850e9014d324
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153267439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b1656c8d38697ccc81c85e5452a5a77ab3df2cbb71e1480c559ab69bfd7ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 10:01:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 10:39:12 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 10:40:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 10:40:46 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 10:42:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 10:42:15 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 10:42:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 10:42:19 GMT
CMD ["node"]
# Fri, 22 Apr 2022 06:04:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 06:06:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 06:06:18 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 06:06:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 06:07:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 06:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 06:07:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 06:07:43 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 06:30:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 06:30:27 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 06:30:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 06:30:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 06:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 06:30:39 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 06:30:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dfd14f4b8dc5b2ece2300878fcb7f82a6c028640285e84df9d6b867d304b4`  
		Last Modified: Thu, 21 Apr 2022 12:45:37 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143b653e4afbc934d43808504513179596c43bcec6c5829b90aefa2a1655141c`  
		Last Modified: Thu, 21 Apr 2022 12:53:08 GMT  
		Size: 38.0 MB (37978299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7cab81867ac00e75a2224d1e0490e517d64a3c4722aa5cff6362296128f7e`  
		Last Modified: Thu, 21 Apr 2022 12:53:01 GMT  
		Size: 2.8 MB (2782412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3d94cf42096de509ac7f5188746e392eddc10a896233407fba98c7562dc9b`  
		Last Modified: Thu, 21 Apr 2022 12:53:00 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816ff917e2908244ff376fc99bc2f36f217a87ed39e8a423e1760a39acc4d973`  
		Last Modified: Fri, 22 Apr 2022 06:31:05 GMT  
		Size: 1.4 MB (1367679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7e8e32f1a52d3e639bccec6487d07e284dcc10a329b69899c14f54e4dfec7`  
		Last Modified: Fri, 22 Apr 2022 06:31:08 GMT  
		Size: 9.6 MB (9570563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54015f599eadbda12c0d070716b0be17e84831d918e0f530c7cd7f777fb40e0b`  
		Last Modified: Fri, 22 Apr 2022 06:31:22 GMT  
		Size: 66.3 MB (66278049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b08801e1ffbcd8cd4bad9689d2bd560716bb5a6da42590ccf4f83289b618ff`  
		Last Modified: Fri, 22 Apr 2022 06:31:04 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0` - linux; s390x

```console
$ docker pull ghost@sha256:7dae1128c62949f7a1f6737c76f4cbaa620dd9ddda262aae0877989c670725eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145197955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df5b85a7a7075af8411748f327feca767a8d03287b304696c6179683f60a711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 13:03:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 13:10:46 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 13:11:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 13:11:13 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 13:11:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 13:11:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 13:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 13:11:24 GMT
CMD ["node"]
# Thu, 21 Apr 2022 07:15:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 07:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 07:15:37 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 00:03:55 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 00:05:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 00:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 00:21:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 00:22:08 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 00:22:08 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 00:22:09 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 00:22:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 00:22:09 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 00:22:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba080336cdb91a025d29d9b1a959402f181ed47358c5aabfe2baa9fbbdb2526`  
		Last Modified: Wed, 20 Apr 2022 13:21:37 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925bee1f31b092e56dc94873158d55cb00cd86545b7aac56ef6a494a1914dc16`  
		Last Modified: Wed, 20 Apr 2022 13:25:04 GMT  
		Size: 35.9 MB (35913825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100515451ae271e479c404cf7ad8b5bd8ac5b200fb51b3549c392338843d51c4`  
		Last Modified: Wed, 20 Apr 2022 13:25:00 GMT  
		Size: 2.8 MB (2783085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33294f3eb8fb473f81134c1152e757722051c32cd70ab61f26397f548d16d9ad`  
		Last Modified: Wed, 20 Apr 2022 13:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0219c13a23e2876d5d7e61f468c0af6df28544c16e3b91297ceabd2e0d4f7`  
		Last Modified: Thu, 21 Apr 2022 07:19:46 GMT  
		Size: 1.4 MB (1435082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edb84d1f4bcc5228531be258c5e5fb559211e773ea04528ef9646faea2f3f9`  
		Last Modified: Fri, 22 Apr 2022 00:22:41 GMT  
		Size: 9.6 MB (9570616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b0ae9fc8a5c17363e53126553ef9e33748dbc990389ee3b0d1e7975ef7717`  
		Last Modified: Fri, 22 Apr 2022 00:22:50 GMT  
		Size: 65.8 MB (65835359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28594230d81842fb65dd01ee7dcfda86421a415f56510caf408464cd231c23`  
		Last Modified: Fri, 22 Apr 2022 00:22:39 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.44.0-alpine`

```console
$ docker pull ghost@sha256:09157352e9ea076529679e7d31b13bd6569408731f93945a3cf9f05600453e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4.44.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:df796a02fd7cf35870d8d28d2956f3b7eee84d108f346c4f072bac87699e0cad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123093602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2a36dee5865a44db3568de3ec4073800e9d55d4529cc42419fbadcc962a93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:11:16 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 10:11:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 10:11:25 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 10:11:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 10:11:30 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:11:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 10:11:30 GMT
CMD ["node"]
# Tue, 05 Apr 2022 15:54:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 15:54:31 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 15:54:31 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:25:28 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:25:51 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:25:51 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:28:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:28:52 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:28:52 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:28:52 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 22:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:28:52 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:28:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f77dc7475a9ee1adc8d2d5488f32f32738586bd2d990b8e1caa80544a30572`  
		Last Modified: Tue, 05 Apr 2022 10:18:09 GMT  
		Size: 37.1 MB (37132761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0229f3f8988db17639cba0c34bf5b284794200e08a64b2e7e8d1e2a951a42dbf`  
		Last Modified: Tue, 05 Apr 2022 10:18:04 GMT  
		Size: 2.4 MB (2358380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ba6c2a71cc186b7d902e57a76b3ab2839273e293f35edf69dfc28a4e7fc864`  
		Last Modified: Tue, 05 Apr 2022 10:18:03 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ce844d16ce9093f01a858beb09d6ea6b265045575d2e17a8332bd5a24cc16`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac48c6254796bcd50706c0855803821724adfb9870c4a5e81aaf7d85b86ddfb0`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 817.2 KB (817176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af283bf213bc2ff10d2387b35dcf2e46b595ef162af50d0ee6f82f712108c5f`  
		Last Modified: Thu, 21 Apr 2022 22:29:47 GMT  
		Size: 9.6 MB (9570321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfed21aca3ad21d702b547fc250ebf1e5fa1d7d24b350a445e01d089b0d2c98`  
		Last Modified: Thu, 21 Apr 2022 22:29:57 GMT  
		Size: 70.4 MB (70384385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ebcadede294e08bf68ebdeb776b89260dbe3bbaadc5cb24720ac86a198e72`  
		Last Modified: Thu, 21 Apr 2022 22:29:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:230bec2aef8fa0cd397c4f7f5c9709761bdc598d8509dac6700fbb9909e73beb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115333582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56781ad6b302e62f470137103ccf7f07728f8274d842347fe0518104e3fa49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:26:29 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 05:40:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 05:40:06 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 05:40:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 05:40:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 05:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 05:40:15 GMT
CMD ["node"]
# Tue, 05 Apr 2022 18:24:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 18:24:40 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 18:24:40 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:49:35 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:50:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:50:51 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:00:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:00:10 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:00:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:00:11 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:00:12 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:00:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3354dc99866b12a88c4bd7ed711488887cbed01d841e9794c65e7592cead0e42`  
		Last Modified: Tue, 05 Apr 2022 06:36:00 GMT  
		Size: 36.2 MB (36198138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1a58fa44a08ad15f35491309df29537157889803b60be33bdcb0664e2a587f`  
		Last Modified: Tue, 05 Apr 2022 06:35:36 GMT  
		Size: 2.4 MB (2418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d8ebe696986f6652a7ed3c86ac8ba3793d5119d8afd3b128a1e9a18cb70c1`  
		Last Modified: Tue, 05 Apr 2022 06:35:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61091aa7bda313caca280046e5231603b20ac0bf519ec7c8660178bd8c2f9d44`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 11.0 KB (10974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633c6d790ae1e67a13d13aca30e70be2f0eae095032a15f16a6c85414b0f669`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 771.2 KB (771175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ff3529d9e58c2564925c042f63c2955a6cc649aea978bf0933966ee357b55a`  
		Last Modified: Thu, 21 Apr 2022 23:01:07 GMT  
		Size: 9.6 MB (9570632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08f662c1d4c2beef8d944f6bab58a6b3ebb1f758e824e540c4d243a1107f68`  
		Last Modified: Thu, 21 Apr 2022 23:01:48 GMT  
		Size: 63.7 MB (63737150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba68ac064a5e907fdebb93f13a85c4ce6553bbf26724b085d4fb39924965fad`  
		Last Modified: Thu, 21 Apr 2022 23:00:52 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b726c091588289db1bbdea4ac9cd4a1fedcfd37fb93280fbfd124113fd86a4d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114164496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee1d6d1cc42b5a325acdb33dcd4c3ce5c5bb2f83335ed46f7533fca22cbe3e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 17:43:03 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 17:55:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 17:55:54 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 17:56:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 17:56:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 17:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 17:56:03 GMT
CMD ["node"]
# Wed, 06 Apr 2022 02:45:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 06 Apr 2022 02:45:39 GMT
RUN apk add --no-cache 		bash
# Wed, 06 Apr 2022 02:45:39 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:51:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:52:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:52:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:59:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:59:17 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:59:18 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:59:18 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Apr 2022 12:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:59:19 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:59:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3df1e2806696dbaefd6243268e71b96d0bcc55e4e0200bb608e50e9472b720`  
		Last Modified: Tue, 05 Apr 2022 19:02:58 GMT  
		Size: 35.8 MB (35751067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09205dfcd8b25ca660d2dfd77d64e8e49af76687cccba75fbb7f876e77c393b0`  
		Last Modified: Tue, 05 Apr 2022 19:02:36 GMT  
		Size: 2.4 MB (2418454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e036f8d684cce25c16a09e061c8bff2abdbea00d775921960e82a7522cef2`  
		Last Modified: Tue, 05 Apr 2022 19:02:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251af54f86884a25fdd443f42b9a4b98657feca7ec58c23906c88699d006b556`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 10.8 KB (10770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46253eacab6b15a2fa733739521d11aa8347847dfd13258a776db2356f6c44`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 704.1 KB (704134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1df2bbc6958308178c27d7394faecd48ebc5d931de77dc4fc206693140028`  
		Last Modified: Fri, 22 Apr 2022 13:02:01 GMT  
		Size: 9.6 MB (9570602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1d6a69a41962a4b57a309945b871f09d7221da8e489b20fff26326ba745a38`  
		Last Modified: Fri, 22 Apr 2022 13:02:52 GMT  
		Size: 63.3 MB (63280500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5a8e6f14e8f948f86787b1b667c57bcac324f97cb8b4895c99d7f4e8b71e7`  
		Last Modified: Fri, 22 Apr 2022 13:01:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.44.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e080be80d222d9f3a99a535ca1f8919e481805fd00cf8217be64e32ec214b746
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133741681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7423f42d5f279e76f5ccb7054acc2d966aa76b459b8421d57b7040f1351d7367`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:10:00 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 11:29:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 11:29:56 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 11:30:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 11:30:04 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:30:05 GMT
CMD ["node"]
# Tue, 05 Apr 2022 17:40:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 17:40:56 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 17:40:57 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:04:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:04:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:04:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:04:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:04:48 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:08:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:08:29 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:08:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:08:34 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:08:39 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:08:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10981ae1a586f08fc64f5e03af14d53d489f3d7762b11a35f4e0e650a871f3b`  
		Last Modified: Tue, 05 Apr 2022 14:16:18 GMT  
		Size: 37.0 MB (37013669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379155faf1aa767ddbc2287fb89a7a8dcead27019d96b6b2046649ee936df951`  
		Last Modified: Tue, 05 Apr 2022 14:16:12 GMT  
		Size: 2.4 MB (2425558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c4fa407cbf0ddea9951284ad9e593b19f9158ee60f6ae61868b179698a75cd`  
		Last Modified: Tue, 05 Apr 2022 14:16:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f79cb613167b8dc819ee3651e614a3b07f5182f73fd37f990f92075b6dfc7f`  
		Last Modified: Tue, 05 Apr 2022 17:45:58 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea380f558fd6b4eecfa37b880e2d489e98e7ebe10d366ef0004f1ef3f3b16ce`  
		Last Modified: Tue, 05 Apr 2022 17:45:59 GMT  
		Size: 826.3 KB (826295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcffbbf76d14f11471479d15f5b7eed819189fd961749b0be7134aa472a3922b`  
		Last Modified: Thu, 21 Apr 2022 23:09:40 GMT  
		Size: 9.6 MB (9570230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2717e5cf0c28b9bb7dca8e07c7ccf5cd52aa4f0f381b0ca1742001ca47f028`  
		Last Modified: Thu, 21 Apr 2022 23:09:52 GMT  
		Size: 81.2 MB (81176546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8239852696e954fa3520fb4475ef4715eaadb69d9abf4ace59f267953fb4bb30`  
		Last Modified: Thu, 21 Apr 2022 23:09:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:09157352e9ea076529679e7d31b13bd6569408731f93945a3cf9f05600453e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:df796a02fd7cf35870d8d28d2956f3b7eee84d108f346c4f072bac87699e0cad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123093602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2a36dee5865a44db3568de3ec4073800e9d55d4529cc42419fbadcc962a93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:11:16 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 10:11:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 10:11:25 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 10:11:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 10:11:30 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:11:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 10:11:30 GMT
CMD ["node"]
# Tue, 05 Apr 2022 15:54:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 15:54:31 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 15:54:31 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:25:28 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:25:51 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:25:51 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:25:52 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:28:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:28:52 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:28:52 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:28:52 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 22:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:28:52 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:28:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f77dc7475a9ee1adc8d2d5488f32f32738586bd2d990b8e1caa80544a30572`  
		Last Modified: Tue, 05 Apr 2022 10:18:09 GMT  
		Size: 37.1 MB (37132761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0229f3f8988db17639cba0c34bf5b284794200e08a64b2e7e8d1e2a951a42dbf`  
		Last Modified: Tue, 05 Apr 2022 10:18:04 GMT  
		Size: 2.4 MB (2358380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ba6c2a71cc186b7d902e57a76b3ab2839273e293f35edf69dfc28a4e7fc864`  
		Last Modified: Tue, 05 Apr 2022 10:18:03 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ce844d16ce9093f01a858beb09d6ea6b265045575d2e17a8332bd5a24cc16`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac48c6254796bcd50706c0855803821724adfb9870c4a5e81aaf7d85b86ddfb0`  
		Last Modified: Tue, 05 Apr 2022 15:56:20 GMT  
		Size: 817.2 KB (817176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af283bf213bc2ff10d2387b35dcf2e46b595ef162af50d0ee6f82f712108c5f`  
		Last Modified: Thu, 21 Apr 2022 22:29:47 GMT  
		Size: 9.6 MB (9570321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfed21aca3ad21d702b547fc250ebf1e5fa1d7d24b350a445e01d089b0d2c98`  
		Last Modified: Thu, 21 Apr 2022 22:29:57 GMT  
		Size: 70.4 MB (70384385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ebcadede294e08bf68ebdeb776b89260dbe3bbaadc5cb24720ac86a198e72`  
		Last Modified: Thu, 21 Apr 2022 22:29:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:230bec2aef8fa0cd397c4f7f5c9709761bdc598d8509dac6700fbb9909e73beb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115333582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56781ad6b302e62f470137103ccf7f07728f8274d842347fe0518104e3fa49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:26:29 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 05:40:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 05:40:06 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 05:40:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 05:40:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 05:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 05:40:15 GMT
CMD ["node"]
# Tue, 05 Apr 2022 18:24:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 18:24:40 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 18:24:40 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:49:35 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:50:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:50:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:50:51 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:00:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:00:10 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:00:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:00:11 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:00:12 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:00:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3354dc99866b12a88c4bd7ed711488887cbed01d841e9794c65e7592cead0e42`  
		Last Modified: Tue, 05 Apr 2022 06:36:00 GMT  
		Size: 36.2 MB (36198138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1a58fa44a08ad15f35491309df29537157889803b60be33bdcb0664e2a587f`  
		Last Modified: Tue, 05 Apr 2022 06:35:36 GMT  
		Size: 2.4 MB (2418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d8ebe696986f6652a7ed3c86ac8ba3793d5119d8afd3b128a1e9a18cb70c1`  
		Last Modified: Tue, 05 Apr 2022 06:35:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61091aa7bda313caca280046e5231603b20ac0bf519ec7c8660178bd8c2f9d44`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 11.0 KB (10974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633c6d790ae1e67a13d13aca30e70be2f0eae095032a15f16a6c85414b0f669`  
		Last Modified: Tue, 05 Apr 2022 18:36:24 GMT  
		Size: 771.2 KB (771175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ff3529d9e58c2564925c042f63c2955a6cc649aea978bf0933966ee357b55a`  
		Last Modified: Thu, 21 Apr 2022 23:01:07 GMT  
		Size: 9.6 MB (9570632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08f662c1d4c2beef8d944f6bab58a6b3ebb1f758e824e540c4d243a1107f68`  
		Last Modified: Thu, 21 Apr 2022 23:01:48 GMT  
		Size: 63.7 MB (63737150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba68ac064a5e907fdebb93f13a85c4ce6553bbf26724b085d4fb39924965fad`  
		Last Modified: Thu, 21 Apr 2022 23:00:52 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:b726c091588289db1bbdea4ac9cd4a1fedcfd37fb93280fbfd124113fd86a4d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114164496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee1d6d1cc42b5a325acdb33dcd4c3ce5c5bb2f83335ed46f7533fca22cbe3e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 17:43:03 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 17:55:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 17:55:54 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 17:56:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 17:56:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 17:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 17:56:03 GMT
CMD ["node"]
# Wed, 06 Apr 2022 02:45:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 06 Apr 2022 02:45:39 GMT
RUN apk add --no-cache 		bash
# Wed, 06 Apr 2022 02:45:39 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:51:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:52:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:52:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:52:14 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:59:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:59:17 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:59:18 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:59:18 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Apr 2022 12:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:59:19 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:59:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3df1e2806696dbaefd6243268e71b96d0bcc55e4e0200bb608e50e9472b720`  
		Last Modified: Tue, 05 Apr 2022 19:02:58 GMT  
		Size: 35.8 MB (35751067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09205dfcd8b25ca660d2dfd77d64e8e49af76687cccba75fbb7f876e77c393b0`  
		Last Modified: Tue, 05 Apr 2022 19:02:36 GMT  
		Size: 2.4 MB (2418454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e036f8d684cce25c16a09e061c8bff2abdbea00d775921960e82a7522cef2`  
		Last Modified: Tue, 05 Apr 2022 19:02:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251af54f86884a25fdd443f42b9a4b98657feca7ec58c23906c88699d006b556`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 10.8 KB (10770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46253eacab6b15a2fa733739521d11aa8347847dfd13258a776db2356f6c44`  
		Last Modified: Wed, 06 Apr 2022 02:54:57 GMT  
		Size: 704.1 KB (704134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f1df2bbc6958308178c27d7394faecd48ebc5d931de77dc4fc206693140028`  
		Last Modified: Fri, 22 Apr 2022 13:02:01 GMT  
		Size: 9.6 MB (9570602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1d6a69a41962a4b57a309945b871f09d7221da8e489b20fff26326ba745a38`  
		Last Modified: Fri, 22 Apr 2022 13:02:52 GMT  
		Size: 63.3 MB (63280500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5a8e6f14e8f948f86787b1b667c57bcac324f97cb8b4895c99d7f4e8b71e7`  
		Last Modified: Fri, 22 Apr 2022 13:01:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e080be80d222d9f3a99a535ca1f8919e481805fd00cf8217be64e32ec214b746
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133741681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7423f42d5f279e76f5ccb7054acc2d966aa76b459b8421d57b7040f1351d7367`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:10:00 GMT
ENV NODE_VERSION=14.19.1
# Tue, 05 Apr 2022 11:29:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 05 Apr 2022 11:29:56 GMT
ENV YARN_VERSION=1.22.17
# Tue, 05 Apr 2022 11:30:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 05 Apr 2022 11:30:04 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:30:05 GMT
CMD ["node"]
# Tue, 05 Apr 2022 17:40:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 17:40:56 GMT
RUN apk add --no-cache 		bash
# Tue, 05 Apr 2022 17:40:57 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:04:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:04:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:04:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:04:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:04:48 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:08:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:08:29 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:08:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:08:34 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 21 Apr 2022 23:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:08:39 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:08:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10981ae1a586f08fc64f5e03af14d53d489f3d7762b11a35f4e0e650a871f3b`  
		Last Modified: Tue, 05 Apr 2022 14:16:18 GMT  
		Size: 37.0 MB (37013669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379155faf1aa767ddbc2287fb89a7a8dcead27019d96b6b2046649ee936df951`  
		Last Modified: Tue, 05 Apr 2022 14:16:12 GMT  
		Size: 2.4 MB (2425558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c4fa407cbf0ddea9951284ad9e593b19f9158ee60f6ae61868b179698a75cd`  
		Last Modified: Tue, 05 Apr 2022 14:16:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f79cb613167b8dc819ee3651e614a3b07f5182f73fd37f990f92075b6dfc7f`  
		Last Modified: Tue, 05 Apr 2022 17:45:58 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea380f558fd6b4eecfa37b880e2d489e98e7ebe10d366ef0004f1ef3f3b16ce`  
		Last Modified: Tue, 05 Apr 2022 17:45:59 GMT  
		Size: 826.3 KB (826295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcffbbf76d14f11471479d15f5b7eed819189fd961749b0be7134aa472a3922b`  
		Last Modified: Thu, 21 Apr 2022 23:09:40 GMT  
		Size: 9.6 MB (9570230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2717e5cf0c28b9bb7dca8e07c7ccf5cd52aa4f0f381b0ca1742001ca47f028`  
		Last Modified: Thu, 21 Apr 2022 23:09:52 GMT  
		Size: 81.2 MB (81176546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8239852696e954fa3520fb4475ef4715eaadb69d9abf4ace59f267953fb4bb30`  
		Last Modified: Thu, 21 Apr 2022 23:09:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:29ae24acabf010c1c4b41f5150f3b452cbcbaa13d6b4fdd84acdc41a7c860751
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
$ docker pull ghost@sha256:dcf72234dc1303677c14bcd1209024f694d24fbf0ed26f865adad6f40d65083c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151543699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cb5dc64a580976014b49b40719a817b63b1ff999fa1fecd6d7a0fb47e10dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:13:21 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 10:21:17 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 10:21:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 10:21:43 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 10:21:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 10:21:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:21:56 GMT
CMD ["node"]
# Thu, 21 Apr 2022 00:11:23 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 00:11:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 00:11:34 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 22:21:50 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 22:22:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 22:22:27 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 22:25:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 22:25:25 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 22:25:25 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 22:25:25 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 22:25:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 22:25:25 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 22:25:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e668081a27339473567eb3eafa1abbd3f5ceefaa67434d1748f8c46d4fdf6f93`  
		Last Modified: Wed, 20 Apr 2022 10:32:04 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d444f00d53b845fef8ee473fc7552d50c5e3e57fbb827950c268765b74fac00`  
		Last Modified: Wed, 20 Apr 2022 10:38:09 GMT  
		Size: 36.0 MB (36048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128a733a96c68606bdf399393f948360adf06c8f764dfdd018ee97787766a580`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 2.8 MB (2782020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e41e9aed24621d2afef40857683cc73a4c4b7f8edafca46393adfde99b2c35`  
		Last Modified: Wed, 20 Apr 2022 10:38:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392af486ff5dbf6170c741891fcebec191cdf0e3c4c259066c793deecd9228d4`  
		Last Modified: Thu, 21 Apr 2022 00:15:29 GMT  
		Size: 1.4 MB (1448178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dceceeb7a32edbf92b0b1774e7c4d8bb5ee7359f152a487336d67d85900f4c8`  
		Last Modified: Thu, 21 Apr 2022 22:29:19 GMT  
		Size: 9.6 MB (9570265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2a24e4ad5d7372fccff886ddb62200a79ccd62b5109fa5fb86b47c1f5da943`  
		Last Modified: Thu, 21 Apr 2022 22:29:29 GMT  
		Size: 70.3 MB (70310984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a61eda0deea4d1392171921a14042695e0ac43122821b03710136c13d48033`  
		Last Modified: Thu, 21 Apr 2022 22:29:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fb63c0d5977b9249d7ab172fd66793968563a6dd7eb9139e1e9ce4367d473b61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154080429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e8fc193382395aeabfb43b785fb9872ab4df1f5cac0753233174175ad00c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 00:10:51 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 00:33:11 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 00:34:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 00:34:02 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 00:34:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 00:34:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 00:34:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 00:34:37 GMT
CMD ["node"]
# Fri, 22 Apr 2022 12:42:04 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 12:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 12:42:33 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 12:42:34 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 12:43:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 12:43:24 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 12:43:25 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 12:51:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 12:51:06 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 12:51:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 12:51:06 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 12:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 12:51:07 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 12:51:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34257bda5d3bc8816a1eb85fb98c52dbadc165802b744fe00e5faddf24f991f`  
		Last Modified: Thu, 21 Apr 2022 01:06:29 GMT  
		Size: 4.2 KB (4175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf55f73d31fce34821ae83bc50b171467d8a58cf9b933beb5934e7d980a8ed`  
		Last Modified: Thu, 21 Apr 2022 01:21:53 GMT  
		Size: 34.2 MB (34206825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd1b29f94636265d9da4c4e338481c420646410fc05c9deb7e5249e35e87e29`  
		Last Modified: Thu, 21 Apr 2022 01:21:31 GMT  
		Size: 2.8 MB (2772510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07331afdbc0a6a01673214e15f644bcea3f093d9eff5f6b229704c0ea423bb94`  
		Last Modified: Thu, 21 Apr 2022 01:21:29 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e1e05156a40d5bce75161ae5f726cf145e05bc9c8fbf34f8c28c1bd183ddc`  
		Last Modified: Fri, 22 Apr 2022 13:00:12 GMT  
		Size: 1.4 MB (1400368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5d91eea624399af581a48ea55e625d0c7cecbdaba19a9dc4e425ea18f826e7`  
		Last Modified: Fri, 22 Apr 2022 13:00:26 GMT  
		Size: 9.6 MB (9570576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeabdf632b0c643c388782fa3e87b2008897f032edabb392eeb5ac9f741ec54`  
		Last Modified: Fri, 22 Apr 2022 13:01:25 GMT  
		Size: 79.5 MB (79549224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c9f209a2361c029ddd688a21a6c7fd3e5a7bcf952ead5b3eb23a7ab14fc491`  
		Last Modified: Fri, 22 Apr 2022 13:00:11 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:9aa8f6209d3c3009663bf6a8aee37577343eb3261e5c1d567a4e3d1cb6ec5e9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161658595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3122dbf6a0293d6db766fe1bfbc1faae9e712cfffd1a9d3291342650203ec789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:46:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 09:56:24 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 09:56:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 09:56:49 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 09:57:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 09:57:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 09:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 09:57:04 GMT
CMD ["node"]
# Thu, 21 Apr 2022 02:54:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 02:54:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 02:54:50 GMT
ENV NODE_ENV=production
# Thu, 21 Apr 2022 23:00:21 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Thu, 21 Apr 2022 23:00:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 21 Apr 2022 23:00:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 21 Apr 2022 23:00:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 21 Apr 2022 23:00:50 GMT
ENV GHOST_VERSION=4.44.0
# Thu, 21 Apr 2022 23:03:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 21 Apr 2022 23:04:00 GMT
WORKDIR /var/lib/ghost
# Thu, 21 Apr 2022 23:04:02 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 21 Apr 2022 23:04:05 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 21 Apr 2022 23:04:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 23:04:10 GMT
EXPOSE 2368
# Thu, 21 Apr 2022 23:04:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcf03983304e3396f5948d3c624e30b772d1ff3509c706caed83ef28438f1da`  
		Last Modified: Wed, 20 Apr 2022 10:11:56 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4805c92d5c569c2f4495e0fd8e12a465f61fc0f5d5f4d89cc220b13ff2557411`  
		Last Modified: Wed, 20 Apr 2022 10:18:24 GMT  
		Size: 36.2 MB (36154398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6f866fefa758cc4823ad299004cbd908ed1c0d073b1004bf0b72f215c84828`  
		Last Modified: Wed, 20 Apr 2022 10:18:18 GMT  
		Size: 2.8 MB (2781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19f3a7274e477fc771ea00030f1c865c9a10c3e38e7aeb6be2d8a08599a25a`  
		Last Modified: Wed, 20 Apr 2022 10:18:17 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e79b5da82b9c170dd4b8cf196aab0fcc967a59ecf812e15dd5449b29d177fa9`  
		Last Modified: Thu, 21 Apr 2022 02:59:29 GMT  
		Size: 1.4 MB (1383713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2d9987c1e1828a89a66e4e776001ab45a14c9d3ac25ab5934cf0ee39ae70e`  
		Last Modified: Thu, 21 Apr 2022 23:09:08 GMT  
		Size: 9.6 MB (9570279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ca43bc7c56fb596b5bb021ee79aab4a7727b286c905cc83755dafbf56ba72`  
		Last Modified: Thu, 21 Apr 2022 23:09:20 GMT  
		Size: 81.7 MB (81697963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55adc76500a79cce32120afe64e6738e37cbd42204e03d7984ffa7733348869e`  
		Last Modified: Thu, 21 Apr 2022 23:09:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:97cd1d65c37e5ff12351986abeadc8410445d54ebef0b20c8f5c850e9014d324
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153267439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b1656c8d38697ccc81c85e5452a5a77ab3df2cbb71e1480c559ab69bfd7ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 10:01:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 21 Apr 2022 10:39:12 GMT
ENV NODE_VERSION=14.19.1
# Thu, 21 Apr 2022 10:40:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 21 Apr 2022 10:40:46 GMT
ENV YARN_VERSION=1.22.17
# Thu, 21 Apr 2022 10:42:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 21 Apr 2022 10:42:15 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 21 Apr 2022 10:42:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 10:42:19 GMT
CMD ["node"]
# Fri, 22 Apr 2022 06:04:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 22 Apr 2022 06:06:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 06:06:18 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 06:06:19 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 06:07:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 06:07:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 06:07:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 06:07:43 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 06:30:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 06:30:27 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 06:30:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 06:30:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 06:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 06:30:39 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 06:30:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dfd14f4b8dc5b2ece2300878fcb7f82a6c028640285e84df9d6b867d304b4`  
		Last Modified: Thu, 21 Apr 2022 12:45:37 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143b653e4afbc934d43808504513179596c43bcec6c5829b90aefa2a1655141c`  
		Last Modified: Thu, 21 Apr 2022 12:53:08 GMT  
		Size: 38.0 MB (37978299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7cab81867ac00e75a2224d1e0490e517d64a3c4722aa5cff6362296128f7e`  
		Last Modified: Thu, 21 Apr 2022 12:53:01 GMT  
		Size: 2.8 MB (2782412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3d94cf42096de509ac7f5188746e392eddc10a896233407fba98c7562dc9b`  
		Last Modified: Thu, 21 Apr 2022 12:53:00 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816ff917e2908244ff376fc99bc2f36f217a87ed39e8a423e1760a39acc4d973`  
		Last Modified: Fri, 22 Apr 2022 06:31:05 GMT  
		Size: 1.4 MB (1367679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7e8e32f1a52d3e639bccec6487d07e284dcc10a329b69899c14f54e4dfec7`  
		Last Modified: Fri, 22 Apr 2022 06:31:08 GMT  
		Size: 9.6 MB (9570563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54015f599eadbda12c0d070716b0be17e84831d918e0f530c7cd7f777fb40e0b`  
		Last Modified: Fri, 22 Apr 2022 06:31:22 GMT  
		Size: 66.3 MB (66278049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b08801e1ffbcd8cd4bad9689d2bd560716bb5a6da42590ccf4f83289b618ff`  
		Last Modified: Fri, 22 Apr 2022 06:31:04 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:7dae1128c62949f7a1f6737c76f4cbaa620dd9ddda262aae0877989c670725eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145197955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df5b85a7a7075af8411748f327feca767a8d03287b304696c6179683f60a711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 13:03:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 20 Apr 2022 13:10:46 GMT
ENV NODE_VERSION=14.19.1
# Wed, 20 Apr 2022 13:11:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Wed, 20 Apr 2022 13:11:13 GMT
ENV YARN_VERSION=1.22.17
# Wed, 20 Apr 2022 13:11:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Wed, 20 Apr 2022 13:11:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 20 Apr 2022 13:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 13:11:24 GMT
CMD ["node"]
# Thu, 21 Apr 2022 07:15:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Apr 2022 07:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 07:15:37 GMT
ENV NODE_ENV=production
# Fri, 22 Apr 2022 00:03:55 GMT
ENV GHOST_CLI_VERSION=1.19.3
# Fri, 22 Apr 2022 00:05:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Apr 2022 00:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Apr 2022 00:05:17 GMT
ENV GHOST_VERSION=4.44.0
# Fri, 22 Apr 2022 00:21:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies["@vscode/sqlite3"]')"; 	[ -n "$sqlite3Version" ]; 	[ "$sqlite3Version" != 'undefined' ]; 	if ! gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python2; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python2' gosu node yarn add "@vscode/sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Apr 2022 00:22:08 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Apr 2022 00:22:08 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Apr 2022 00:22:09 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 22 Apr 2022 00:22:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 00:22:09 GMT
EXPOSE 2368
# Fri, 22 Apr 2022 00:22:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba080336cdb91a025d29d9b1a959402f181ed47358c5aabfe2baa9fbbdb2526`  
		Last Modified: Wed, 20 Apr 2022 13:21:37 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925bee1f31b092e56dc94873158d55cb00cd86545b7aac56ef6a494a1914dc16`  
		Last Modified: Wed, 20 Apr 2022 13:25:04 GMT  
		Size: 35.9 MB (35913825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100515451ae271e479c404cf7ad8b5bd8ac5b200fb51b3549c392338843d51c4`  
		Last Modified: Wed, 20 Apr 2022 13:25:00 GMT  
		Size: 2.8 MB (2783085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33294f3eb8fb473f81134c1152e757722051c32cd70ab61f26397f548d16d9ad`  
		Last Modified: Wed, 20 Apr 2022 13:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0219c13a23e2876d5d7e61f468c0af6df28544c16e3b91297ceabd2e0d4f7`  
		Last Modified: Thu, 21 Apr 2022 07:19:46 GMT  
		Size: 1.4 MB (1435082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edb84d1f4bcc5228531be258c5e5fb559211e773ea04528ef9646faea2f3f9`  
		Last Modified: Fri, 22 Apr 2022 00:22:41 GMT  
		Size: 9.6 MB (9570616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b0ae9fc8a5c17363e53126553ef9e33748dbc990389ee3b0d1e7975ef7717`  
		Last Modified: Fri, 22 Apr 2022 00:22:50 GMT  
		Size: 65.8 MB (65835359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28594230d81842fb65dd01ee7dcfda86421a415f56510caf408464cd231c23`  
		Last Modified: Fri, 22 Apr 2022 00:22:39 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

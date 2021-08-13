<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:3`](#ghost3)
-	[`ghost:3-alpine`](#ghost3-alpine)
-	[`ghost:3.42`](#ghost342)
-	[`ghost:3.42-alpine`](#ghost342-alpine)
-	[`ghost:3.42.5`](#ghost3425)
-	[`ghost:3.42.5-alpine`](#ghost3425-alpine)
-	[`ghost:4`](#ghost4)
-	[`ghost:4-alpine`](#ghost4-alpine)
-	[`ghost:4.11`](#ghost411)
-	[`ghost:4.11-alpine`](#ghost411-alpine)
-	[`ghost:4.11.0`](#ghost4110)
-	[`ghost:4.11.0-alpine`](#ghost4110-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:3`

```console
$ docker pull ghost@sha256:3458dd98a6b39da644741713993c26ddef0add1a175408b4e5688113536b4882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:3` - linux; amd64

```console
$ docker pull ghost@sha256:cf569e68b046c86bd1489cf7590e1fce2abc172b52ffd308b1630d51d5abeadb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134596069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2018be159de67b6c3e8255e1668f0a99ad25660114c6d3830a3b21dfecdf99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:29:34 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 18:29:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:29:59 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:30:13 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:30:13 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:30:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:30:13 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:05:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:05:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:05:49 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:05:49 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:06:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_VERSION=3.42.5
# Thu, 12 Aug 2021 19:07:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:07:26 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:07:26 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:07:26 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:07:27 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:07:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898470a632a79ae16e4ea22c47f9e9975540952b925f81c1ba43f03b85e8664b`  
		Last Modified: Thu, 12 Aug 2021 18:44:24 GMT  
		Size: 24.1 MB (24085481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8450ead35388e1677754e1c319fd3f3462f6a8a647974f7218e5369157b254`  
		Last Modified: Thu, 12 Aug 2021 18:44:21 GMT  
		Size: 2.7 MB (2732673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fc3fe1c99886a85c41d2ba3fe143b30b347990fc8e164d10a4c91c52fa4858`  
		Last Modified: Thu, 12 Aug 2021 18:44:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957351c07eb33669ef5c578947c1b2fa8637657978f356004e61b78be9829370`  
		Last Modified: Thu, 12 Aug 2021 19:10:31 GMT  
		Size: 1.4 MB (1417769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7fcb63dedd0f683f805dad6b4749d8a9ccfacd079794728781456ebe5f3bd`  
		Last Modified: Thu, 12 Aug 2021 19:10:33 GMT  
		Size: 9.4 MB (9403232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b186d95582b7f2c202936c7e5fa087fc357dcd2f2b95fcf4b19822891ff0a0b`  
		Last Modified: Thu, 12 Aug 2021 19:10:44 GMT  
		Size: 69.8 MB (69806109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543acde8e5d7f1cc90b9344c17e4cf4692792049d68131988793b1c68ccc73e`  
		Last Modified: Thu, 12 Aug 2021 19:10:30 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6ae1da20c063947cced09004ccfdf852de5a0e57f95d3d46569af5a5209dc80e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130033887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd965cf8e32c6457235833195e846bb963ab3d266b33410ae27ce45094e2bcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:07:00 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 00:07:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:07:51 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:08:25 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:08:26 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:08:27 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:36:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:36:47 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:36:47 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:37:29 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:37:30 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:37:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:37:31 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 08:44:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:44:59 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:45:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:45:00 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:45:01 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:45:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7db126ab438449a8bcf711971bc4deab9df4d3e95a63695935ee8ec9a5967c`  
		Last Modified: Fri, 13 Aug 2021 00:40:55 GMT  
		Size: 22.1 MB (22098693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c9a84de4e74befb623de090a65ff6587798ee25784d07a82c2576520609cf`  
		Last Modified: Fri, 13 Aug 2021 00:40:40 GMT  
		Size: 2.7 MB (2722750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09202bcb411b3332eafda7b1e253a93da633dee9af1918ae123e86f7e372d7`  
		Last Modified: Fri, 13 Aug 2021 00:40:38 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c37c446e44e9fba2c95433f4153d3e27ed5022dfcec70df7cb481851d5b640`  
		Last Modified: Fri, 13 Aug 2021 08:54:57 GMT  
		Size: 1.4 MB (1370027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1c9f1ee47bed50e701744b9c034a650eabfd6273d1176246cacf3fba1072ff`  
		Last Modified: Fri, 13 Aug 2021 08:55:11 GMT  
		Size: 9.4 MB (9403133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff40cf01a277693ae40fd1e12668ebc263eb6875b6fd527df8d9a293cb64220`  
		Last Modified: Fri, 13 Aug 2021 08:56:16 GMT  
		Size: 71.7 MB (71688300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7288fe54a2cdb9e7c3ca762225a2dd7f58da1461fbf371d17adf73301103eb`  
		Last Modified: Fri, 13 Aug 2021 08:54:56 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f8a6de2bfbb90af004ca6d6be620f90092cd64d8b741f10f4b6762622d9ac38d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118468898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36821ec35e7d84ae8bbe5070aa673b2e596c5b50fca2d5fbe7b33e02023a5e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 02:37:33 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 02:37:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 02:37:58 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 02:38:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 02:38:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 02:38:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 02:38:10 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:27:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:27:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:27:37 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:27:37 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:27:58 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 05:31:11 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:31:14 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:31:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:31:14 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:31:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:31:14 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:31:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26340cf10c1677ec31c5ee3b0cb08965c319b225b03cb003546875af641f2aab`  
		Last Modified: Fri, 13 Aug 2021 02:56:15 GMT  
		Size: 24.0 MB (24047327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eacc37cfc88d18feabbe269c22658aedadaab8db5ad63d0e2b6392c852d79fe`  
		Last Modified: Fri, 13 Aug 2021 02:56:11 GMT  
		Size: 2.7 MB (2732685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4520068f7780f46664f5ae4f99bfd975b1a95c54bab31a487065928720d707b`  
		Last Modified: Fri, 13 Aug 2021 02:56:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcb305ca7bd0c471e8000f7ff964f8ff31af8350b2259213ff081deb6557c9c`  
		Last Modified: Fri, 13 Aug 2021 05:36:19 GMT  
		Size: 1.4 MB (1353052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cabd63bd66d56211b3ade8b07afd3995f40a836d05b2cad627ac9dd1b4255`  
		Last Modified: Fri, 13 Aug 2021 05:36:21 GMT  
		Size: 9.4 MB (9403175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50513bee7d53d884f6aa3b08b7b7c599117d37b6ea6f4f939b1102967ab2acd`  
		Last Modified: Fri, 13 Aug 2021 05:36:33 GMT  
		Size: 55.0 MB (55012847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3112c9cda56f6b18bc7b6b5e2026d21583c7a8350a6cd5a229dd77fd4d66d`  
		Last Modified: Fri, 13 Aug 2021 05:36:18 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3` - linux; ppc64le

```console
$ docker pull ghost@sha256:635c4d7f12b1b639e9a16b1bd3b1eb1f5ce242777d2f2f6c09bd461ea869ad8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123925762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1647a15add09885e872de0f57aadd8d4d501c147ab3732de2aedc3e5b7bdcbdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:38:13 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 23:41:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:41:28 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:44:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:44:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:44:28 GMT
CMD ["node"]
# Fri, 13 Aug 2021 04:15:27 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 04:17:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 04:17:56 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 04:18:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 04:19:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 04:19:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 04:19:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 04:19:13 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 04:45:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:45:29 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:45:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:45:41 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991fe4a926e7cbbf8018cba4b4620c7ae60a970a1f21bcc5a14a0cf9172eaed2`  
		Last Modified: Fri, 13 Aug 2021 00:04:09 GMT  
		Size: 23.9 MB (23904766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1088ffa32997d36c1b61a835ad8a9ff25fa215d3969626a759983cdba4976aa8`  
		Last Modified: Fri, 13 Aug 2021 00:04:04 GMT  
		Size: 2.7 MB (2733492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fd362f0351dc1187856731938aaf1376e0288ed6f0b6bf0a689bdc69a6dbc2`  
		Last Modified: Fri, 13 Aug 2021 00:04:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fb97db4812d407e8d082e574b4e55c8d53822909f2fed45df638654529175`  
		Last Modified: Fri, 13 Aug 2021 04:49:05 GMT  
		Size: 1.3 MB (1338516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f3fa44e0632e353b5af610ba76f42482f2239af4f786212e06c066a2ad5e62`  
		Last Modified: Fri, 13 Aug 2021 04:50:25 GMT  
		Size: 9.4 MB (9403220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c734fbebb843a669e574d8a6e7bf0661a40a5f903f7e95a1bc05df75e618f56`  
		Last Modified: Fri, 13 Aug 2021 04:49:23 GMT  
		Size: 56.0 MB (55987035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55489146a622e3b3db972e92cd327a0f815a6d22deb9320407966cd3aed1c01d`  
		Last Modified: Fri, 13 Aug 2021 04:49:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3` - linux; s390x

```console
$ docker pull ghost@sha256:6e0ae8e0202abd874285b51d1ac7486c3f82d72be3effd9daf9f6e9eb877859b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118476122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720709dd6c6941fe6c538d8fd26597116bec6d8f5955521f104dc74e0b51d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:13:59 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 00:14:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:14:35 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:14:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:14:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:14:54 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:05:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:06:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:06:04 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:06:04 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:06:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:06:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:06:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:06:40 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 03:11:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:11:41 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:11:41 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:11:41 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:11:42 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:11:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3a7258908acb720d296cb0754dddac615f2876d0b9b422867f90c1cfb04df6`  
		Last Modified: Fri, 13 Aug 2021 00:23:39 GMT  
		Size: 24.2 MB (24169257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39fd2cf86fc931078497991d1c069a40f52c846758c59bd0aff46da81fd6485`  
		Last Modified: Fri, 13 Aug 2021 00:23:35 GMT  
		Size: 2.7 MB (2734985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80974528664444037f64e3df3b63d4183dd855fe96d5dbe4f5ce28c5acba1e4`  
		Last Modified: Fri, 13 Aug 2021 00:23:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59981678f3076807402eedf63786632a7b471f2660bb6b61198b9b75e73cb8b1`  
		Last Modified: Fri, 13 Aug 2021 03:12:34 GMT  
		Size: 1.4 MB (1404654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397f70381efd51568fa60e3b543288d48bf5f0954fb68d364f410d9ef1f9ca4c`  
		Last Modified: Fri, 13 Aug 2021 03:12:36 GMT  
		Size: 9.4 MB (9403244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09650d3f76c279b4a99c888df6115c0c13011f438e6b3e22957491a49f946f9`  
		Last Modified: Fri, 13 Aug 2021 03:12:45 GMT  
		Size: 55.0 MB (54998196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbe25f71607668d5a08a56504f56f102456b012981a92578aff198f9f123394`  
		Last Modified: Fri, 13 Aug 2021 03:12:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:3-alpine`

```console
$ docker pull ghost@sha256:3ef07877df2a81cf65f8b5a874584881d00da9fd9b797abc8eed4507d2006112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:3-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1eb63fbf1b030f71441af606f13554e9268634d1955cf990f87fa864b1a250e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110904556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9113d247f1c3c3891f5b5e2cd683ecee3b5e3f6fbaf5febe71af74e9527ac67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:28:27 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 18:28:33 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:28:33 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:28:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:28:37 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:28:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:28:38 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:07:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:07:35 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:07:36 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:07:36 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:07:56 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_VERSION=3.42.5
# Thu, 12 Aug 2021 19:09:04 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:09:07 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:09:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:09:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:09:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:09:07 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:09:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13957d0e312b001d87caca22b0e000f8983402f248ef35e02a184dfcea7a1acb`  
		Last Modified: Thu, 12 Aug 2021 18:42:57 GMT  
		Size: 24.7 MB (24723955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755eebb143c1c9ba699653d6cac3cdbc450ecdcea90612024dcfc08d3c85587c`  
		Last Modified: Thu, 12 Aug 2021 18:42:53 GMT  
		Size: 2.4 MB (2362228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5af900a4f5080da3e57cab4aa7464c4e54f181266075ea05041c67df15e4c63`  
		Last Modified: Thu, 12 Aug 2021 18:42:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775ac215e323ecf0edfc6eaaa0b2620470b24b204f78925d20780c04dcc1e89d`  
		Last Modified: Thu, 12 Aug 2021 19:10:58 GMT  
		Size: 10.1 KB (10069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc2391737d2388dc2178fdd4745064be34a7b3761ee40b7729bbdc09ad847f`  
		Last Modified: Thu, 12 Aug 2021 19:10:59 GMT  
		Size: 779.6 KB (779644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93de3a2a20df8dedf2a3437161acbc2fa1298c85974c9ecee0475f45f496873`  
		Last Modified: Thu, 12 Aug 2021 19:11:01 GMT  
		Size: 9.4 MB (9403191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b081aea7dba6cb43149a4aea518302d8474b645a058ee68aa424ae4b3bd7bd4d`  
		Last Modified: Thu, 12 Aug 2021 19:11:13 GMT  
		Size: 70.8 MB (70824070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98e8d82f3a6e32e1009ca147b4dad078630da13d12227e04e090044351e495`  
		Last Modified: Thu, 12 Aug 2021 19:10:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:924d4776e85cbcefd409d2700a1b818d06ebfb551d6ccac31747d0a8d6c0f39e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94855730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518cf837a7a36e8908a40ce0a10c15853407fa9d280ff0027a571c2d007d616a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:06 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Fri, 30 Jul 2021 17:50:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 22:15:53 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 22:33:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 22:33:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:33:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 22:33:31 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:33:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:33:32 GMT
CMD ["node"]
# Fri, 13 Aug 2021 01:06:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 01:06:54 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 01:06:55 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 01:06:55 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 01:07:52 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 01:16:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 01:16:42 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 01:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 01:16:43 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 01:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:16:44 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 01:16:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a157c308d3669daf8d9e045739a35657c959a5ec42270b7147d4489ee10f57bf`  
		Last Modified: Thu, 12 Aug 2021 23:27:08 GMT  
		Size: 24.2 MB (24151515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdb4bcbb171cbfba72bf8c9715d36edf3949bc8dc58f0e83e835e99ee6a76a3`  
		Last Modified: Thu, 12 Aug 2021 23:26:57 GMT  
		Size: 2.4 MB (2414811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcb2a9161ac2664fc2799ef578a6d193532a670b49414c2fd3920169aa18ba1`  
		Last Modified: Thu, 12 Aug 2021 23:26:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0468520d35faf2e3e34ca95fb3a0b921b9bf74cba5d8e21603c607aad6e6056d`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 9.9 KB (9910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ebfec40337bb10a4a113a5fa394d707e40afa4d54c7834e1b40368c03c8d4b`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 734.0 KB (734013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22f58fb5a660e7280c5c97ac548346933c7d4cab498c786f416d8319635b82d`  
		Last Modified: Fri, 13 Aug 2021 01:17:25 GMT  
		Size: 9.4 MB (9402981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc1231a993aa0298932d54d3487d0e00eea8be3ccb53dd1ec3044df46532a8d`  
		Last Modified: Fri, 13 Aug 2021 01:17:59 GMT  
		Size: 55.5 MB (55536419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243eef57344af5e93f724b40a63171e67c28e5292ab843668e43254a4195bde0`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fccd4feeebf38924f9dbbe08f7d9dd82da67b15c655a65c4b4a134ee10a9a910
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93653630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02a65e5f462767393e652e046387d4213160fb29d7dae0fd51582c4b4ffe052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:56 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Fri, 30 Jul 2021 18:36:57 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 23:19:34 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 23:34:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 23:34:12 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:34:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 23:34:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:34:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:34:21 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 08:45:17 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 08:45:18 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:45:18 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:46:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:46:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:46:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:46:02 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 08:52:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:52:37 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:52:38 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:52:39 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 08:52:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:52:40 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:52:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf136fe6d43db6833f192cab959dd15d2f7ddbd0deb165dbdcf164a1e30df6d`  
		Last Modified: Fri, 13 Aug 2021 00:38:24 GMT  
		Size: 23.7 MB (23708770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a0d668d5c0fecdf6b296d8a6421807cdcaca95f5008271f8ca9d4f25bfd375`  
		Last Modified: Fri, 13 Aug 2021 00:38:08 GMT  
		Size: 2.4 MB (2414693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e162f772f745614305f4ebc6502e61a9dc2bc332144089c3859b36ed24d0487c`  
		Last Modified: Fri, 13 Aug 2021 00:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868398bdc7dd230f3b41eeef84ffe2cdd3eeae867ac01cd345f3ffcb5d9e58db`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2912e9ad030da2a4a90ded28890da15a15d533a041f54c3214571ad6c543b90`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 671.2 KB (671157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd305150da8018a30dabd946fda884c2d2c7f232a01d63d5b0f2475323fb617e`  
		Last Modified: Fri, 13 Aug 2021 08:56:47 GMT  
		Size: 9.4 MB (9403084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c55fb0ce4a71e1354b788b62e1cf5ebe89390a1645236e76dc1099ec4ff05f`  
		Last Modified: Fri, 13 Aug 2021 08:57:46 GMT  
		Size: 55.0 MB (55036232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d255b5196cf6763d0f55dc3dfff03d871e25f64e622c930dbe7be01372008f8`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:844f5c1fcec21acc4f9891ae694f2aac3e619a87ea513474850c5bdc619d27ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95916780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf2953a4f56170338349821197f830071b868242b2917f9ff98a8839a04b9d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:09 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Tue, 15 Jun 2021 21:45:09 GMT
CMD ["/bin/sh"]
# Fri, 13 Aug 2021 01:05:30 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 01:33:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 13 Aug 2021 01:33:37 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 01:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 13 Aug 2021 01:33:43 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 01:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:33:43 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:31:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 05:31:25 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 05:31:25 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:31:25 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:31:48 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:31:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:31:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:31:49 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 05:35:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:35:11 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:35:11 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:35:12 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 05:35:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:35:12 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:35:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c2a5a7092796a92bc42dbed25df2fe05d1e688d8777a5cb4a4463b646f763`  
		Last Modified: Fri, 13 Aug 2021 02:54:43 GMT  
		Size: 24.9 MB (24862053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1296cae68381255931426d96056970c6b17fccbf21bda80ae111106644991b`  
		Last Modified: Fri, 13 Aug 2021 02:54:38 GMT  
		Size: 2.4 MB (2422807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b682014b2cab613154da9269d19af8de7f13125eee5238ec37c80f570f85b`  
		Last Modified: Fri, 13 Aug 2021 02:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ba7ef4dcef81729897900511a18d8ddcd89252fc6b5d22c5fd9dc3d9875662`  
		Last Modified: Fri, 13 Aug 2021 05:36:48 GMT  
		Size: 10.0 KB (10005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91f29270c709a271ba1feab49ffbed6f8c7ae2bdbb47bf463e4ea249e2e435`  
		Last Modified: Fri, 13 Aug 2021 05:36:49 GMT  
		Size: 791.7 KB (791704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f3cd29637fc6b40d14e28bc72dbdf1646e06806a14eb2abf6268e8aa2e4e14`  
		Last Modified: Fri, 13 Aug 2021 05:36:51 GMT  
		Size: 9.4 MB (9403256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee00df371012cfdfc6d7931e01971c404c3f916dfe3d836472e7bc9e7c9cd1`  
		Last Modified: Fri, 13 Aug 2021 05:37:03 GMT  
		Size: 55.7 MB (55715436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e4513517425e2ebf602f7e0cf95689611376d483f289abb0278654e213f9`  
		Last Modified: Fri, 13 Aug 2021 05:36:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:3.42`

```console
$ docker pull ghost@sha256:3458dd98a6b39da644741713993c26ddef0add1a175408b4e5688113536b4882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:3.42` - linux; amd64

```console
$ docker pull ghost@sha256:cf569e68b046c86bd1489cf7590e1fce2abc172b52ffd308b1630d51d5abeadb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134596069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2018be159de67b6c3e8255e1668f0a99ad25660114c6d3830a3b21dfecdf99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:29:34 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 18:29:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:29:59 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:30:13 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:30:13 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:30:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:30:13 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:05:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:05:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:05:49 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:05:49 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:06:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_VERSION=3.42.5
# Thu, 12 Aug 2021 19:07:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:07:26 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:07:26 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:07:26 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:07:27 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:07:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898470a632a79ae16e4ea22c47f9e9975540952b925f81c1ba43f03b85e8664b`  
		Last Modified: Thu, 12 Aug 2021 18:44:24 GMT  
		Size: 24.1 MB (24085481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8450ead35388e1677754e1c319fd3f3462f6a8a647974f7218e5369157b254`  
		Last Modified: Thu, 12 Aug 2021 18:44:21 GMT  
		Size: 2.7 MB (2732673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fc3fe1c99886a85c41d2ba3fe143b30b347990fc8e164d10a4c91c52fa4858`  
		Last Modified: Thu, 12 Aug 2021 18:44:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957351c07eb33669ef5c578947c1b2fa8637657978f356004e61b78be9829370`  
		Last Modified: Thu, 12 Aug 2021 19:10:31 GMT  
		Size: 1.4 MB (1417769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7fcb63dedd0f683f805dad6b4749d8a9ccfacd079794728781456ebe5f3bd`  
		Last Modified: Thu, 12 Aug 2021 19:10:33 GMT  
		Size: 9.4 MB (9403232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b186d95582b7f2c202936c7e5fa087fc357dcd2f2b95fcf4b19822891ff0a0b`  
		Last Modified: Thu, 12 Aug 2021 19:10:44 GMT  
		Size: 69.8 MB (69806109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543acde8e5d7f1cc90b9344c17e4cf4692792049d68131988793b1c68ccc73e`  
		Last Modified: Thu, 12 Aug 2021 19:10:30 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6ae1da20c063947cced09004ccfdf852de5a0e57f95d3d46569af5a5209dc80e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130033887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd965cf8e32c6457235833195e846bb963ab3d266b33410ae27ce45094e2bcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:07:00 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 00:07:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:07:51 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:08:25 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:08:26 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:08:27 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:36:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:36:47 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:36:47 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:37:29 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:37:30 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:37:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:37:31 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 08:44:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:44:59 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:45:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:45:00 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:45:01 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:45:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7db126ab438449a8bcf711971bc4deab9df4d3e95a63695935ee8ec9a5967c`  
		Last Modified: Fri, 13 Aug 2021 00:40:55 GMT  
		Size: 22.1 MB (22098693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c9a84de4e74befb623de090a65ff6587798ee25784d07a82c2576520609cf`  
		Last Modified: Fri, 13 Aug 2021 00:40:40 GMT  
		Size: 2.7 MB (2722750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09202bcb411b3332eafda7b1e253a93da633dee9af1918ae123e86f7e372d7`  
		Last Modified: Fri, 13 Aug 2021 00:40:38 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c37c446e44e9fba2c95433f4153d3e27ed5022dfcec70df7cb481851d5b640`  
		Last Modified: Fri, 13 Aug 2021 08:54:57 GMT  
		Size: 1.4 MB (1370027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1c9f1ee47bed50e701744b9c034a650eabfd6273d1176246cacf3fba1072ff`  
		Last Modified: Fri, 13 Aug 2021 08:55:11 GMT  
		Size: 9.4 MB (9403133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff40cf01a277693ae40fd1e12668ebc263eb6875b6fd527df8d9a293cb64220`  
		Last Modified: Fri, 13 Aug 2021 08:56:16 GMT  
		Size: 71.7 MB (71688300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7288fe54a2cdb9e7c3ca762225a2dd7f58da1461fbf371d17adf73301103eb`  
		Last Modified: Fri, 13 Aug 2021 08:54:56 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f8a6de2bfbb90af004ca6d6be620f90092cd64d8b741f10f4b6762622d9ac38d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118468898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36821ec35e7d84ae8bbe5070aa673b2e596c5b50fca2d5fbe7b33e02023a5e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 02:37:33 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 02:37:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 02:37:58 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 02:38:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 02:38:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 02:38:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 02:38:10 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:27:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:27:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:27:37 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:27:37 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:27:58 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 05:31:11 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:31:14 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:31:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:31:14 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:31:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:31:14 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:31:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26340cf10c1677ec31c5ee3b0cb08965c319b225b03cb003546875af641f2aab`  
		Last Modified: Fri, 13 Aug 2021 02:56:15 GMT  
		Size: 24.0 MB (24047327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eacc37cfc88d18feabbe269c22658aedadaab8db5ad63d0e2b6392c852d79fe`  
		Last Modified: Fri, 13 Aug 2021 02:56:11 GMT  
		Size: 2.7 MB (2732685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4520068f7780f46664f5ae4f99bfd975b1a95c54bab31a487065928720d707b`  
		Last Modified: Fri, 13 Aug 2021 02:56:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcb305ca7bd0c471e8000f7ff964f8ff31af8350b2259213ff081deb6557c9c`  
		Last Modified: Fri, 13 Aug 2021 05:36:19 GMT  
		Size: 1.4 MB (1353052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cabd63bd66d56211b3ade8b07afd3995f40a836d05b2cad627ac9dd1b4255`  
		Last Modified: Fri, 13 Aug 2021 05:36:21 GMT  
		Size: 9.4 MB (9403175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50513bee7d53d884f6aa3b08b7b7c599117d37b6ea6f4f939b1102967ab2acd`  
		Last Modified: Fri, 13 Aug 2021 05:36:33 GMT  
		Size: 55.0 MB (55012847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3112c9cda56f6b18bc7b6b5e2026d21583c7a8350a6cd5a229dd77fd4d66d`  
		Last Modified: Fri, 13 Aug 2021 05:36:18 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42` - linux; ppc64le

```console
$ docker pull ghost@sha256:635c4d7f12b1b639e9a16b1bd3b1eb1f5ce242777d2f2f6c09bd461ea869ad8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123925762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1647a15add09885e872de0f57aadd8d4d501c147ab3732de2aedc3e5b7bdcbdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:38:13 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 23:41:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:41:28 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:44:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:44:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:44:28 GMT
CMD ["node"]
# Fri, 13 Aug 2021 04:15:27 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 04:17:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 04:17:56 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 04:18:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 04:19:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 04:19:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 04:19:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 04:19:13 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 04:45:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:45:29 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:45:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:45:41 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991fe4a926e7cbbf8018cba4b4620c7ae60a970a1f21bcc5a14a0cf9172eaed2`  
		Last Modified: Fri, 13 Aug 2021 00:04:09 GMT  
		Size: 23.9 MB (23904766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1088ffa32997d36c1b61a835ad8a9ff25fa215d3969626a759983cdba4976aa8`  
		Last Modified: Fri, 13 Aug 2021 00:04:04 GMT  
		Size: 2.7 MB (2733492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fd362f0351dc1187856731938aaf1376e0288ed6f0b6bf0a689bdc69a6dbc2`  
		Last Modified: Fri, 13 Aug 2021 00:04:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fb97db4812d407e8d082e574b4e55c8d53822909f2fed45df638654529175`  
		Last Modified: Fri, 13 Aug 2021 04:49:05 GMT  
		Size: 1.3 MB (1338516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f3fa44e0632e353b5af610ba76f42482f2239af4f786212e06c066a2ad5e62`  
		Last Modified: Fri, 13 Aug 2021 04:50:25 GMT  
		Size: 9.4 MB (9403220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c734fbebb843a669e574d8a6e7bf0661a40a5f903f7e95a1bc05df75e618f56`  
		Last Modified: Fri, 13 Aug 2021 04:49:23 GMT  
		Size: 56.0 MB (55987035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55489146a622e3b3db972e92cd327a0f815a6d22deb9320407966cd3aed1c01d`  
		Last Modified: Fri, 13 Aug 2021 04:49:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42` - linux; s390x

```console
$ docker pull ghost@sha256:6e0ae8e0202abd874285b51d1ac7486c3f82d72be3effd9daf9f6e9eb877859b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118476122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720709dd6c6941fe6c538d8fd26597116bec6d8f5955521f104dc74e0b51d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:13:59 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 00:14:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:14:35 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:14:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:14:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:14:54 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:05:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:06:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:06:04 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:06:04 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:06:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:06:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:06:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:06:40 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 03:11:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:11:41 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:11:41 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:11:41 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:11:42 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:11:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3a7258908acb720d296cb0754dddac615f2876d0b9b422867f90c1cfb04df6`  
		Last Modified: Fri, 13 Aug 2021 00:23:39 GMT  
		Size: 24.2 MB (24169257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39fd2cf86fc931078497991d1c069a40f52c846758c59bd0aff46da81fd6485`  
		Last Modified: Fri, 13 Aug 2021 00:23:35 GMT  
		Size: 2.7 MB (2734985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80974528664444037f64e3df3b63d4183dd855fe96d5dbe4f5ce28c5acba1e4`  
		Last Modified: Fri, 13 Aug 2021 00:23:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59981678f3076807402eedf63786632a7b471f2660bb6b61198b9b75e73cb8b1`  
		Last Modified: Fri, 13 Aug 2021 03:12:34 GMT  
		Size: 1.4 MB (1404654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397f70381efd51568fa60e3b543288d48bf5f0954fb68d364f410d9ef1f9ca4c`  
		Last Modified: Fri, 13 Aug 2021 03:12:36 GMT  
		Size: 9.4 MB (9403244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09650d3f76c279b4a99c888df6115c0c13011f438e6b3e22957491a49f946f9`  
		Last Modified: Fri, 13 Aug 2021 03:12:45 GMT  
		Size: 55.0 MB (54998196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbe25f71607668d5a08a56504f56f102456b012981a92578aff198f9f123394`  
		Last Modified: Fri, 13 Aug 2021 03:12:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:3.42-alpine`

```console
$ docker pull ghost@sha256:3ef07877df2a81cf65f8b5a874584881d00da9fd9b797abc8eed4507d2006112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:3.42-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1eb63fbf1b030f71441af606f13554e9268634d1955cf990f87fa864b1a250e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110904556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9113d247f1c3c3891f5b5e2cd683ecee3b5e3f6fbaf5febe71af74e9527ac67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:28:27 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 18:28:33 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:28:33 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:28:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:28:37 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:28:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:28:38 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:07:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:07:35 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:07:36 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:07:36 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:07:56 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_VERSION=3.42.5
# Thu, 12 Aug 2021 19:09:04 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:09:07 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:09:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:09:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:09:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:09:07 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:09:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13957d0e312b001d87caca22b0e000f8983402f248ef35e02a184dfcea7a1acb`  
		Last Modified: Thu, 12 Aug 2021 18:42:57 GMT  
		Size: 24.7 MB (24723955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755eebb143c1c9ba699653d6cac3cdbc450ecdcea90612024dcfc08d3c85587c`  
		Last Modified: Thu, 12 Aug 2021 18:42:53 GMT  
		Size: 2.4 MB (2362228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5af900a4f5080da3e57cab4aa7464c4e54f181266075ea05041c67df15e4c63`  
		Last Modified: Thu, 12 Aug 2021 18:42:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775ac215e323ecf0edfc6eaaa0b2620470b24b204f78925d20780c04dcc1e89d`  
		Last Modified: Thu, 12 Aug 2021 19:10:58 GMT  
		Size: 10.1 KB (10069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc2391737d2388dc2178fdd4745064be34a7b3761ee40b7729bbdc09ad847f`  
		Last Modified: Thu, 12 Aug 2021 19:10:59 GMT  
		Size: 779.6 KB (779644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93de3a2a20df8dedf2a3437161acbc2fa1298c85974c9ecee0475f45f496873`  
		Last Modified: Thu, 12 Aug 2021 19:11:01 GMT  
		Size: 9.4 MB (9403191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b081aea7dba6cb43149a4aea518302d8474b645a058ee68aa424ae4b3bd7bd4d`  
		Last Modified: Thu, 12 Aug 2021 19:11:13 GMT  
		Size: 70.8 MB (70824070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98e8d82f3a6e32e1009ca147b4dad078630da13d12227e04e090044351e495`  
		Last Modified: Thu, 12 Aug 2021 19:10:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:924d4776e85cbcefd409d2700a1b818d06ebfb551d6ccac31747d0a8d6c0f39e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94855730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518cf837a7a36e8908a40ce0a10c15853407fa9d280ff0027a571c2d007d616a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:06 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Fri, 30 Jul 2021 17:50:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 22:15:53 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 22:33:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 22:33:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:33:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 22:33:31 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:33:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:33:32 GMT
CMD ["node"]
# Fri, 13 Aug 2021 01:06:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 01:06:54 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 01:06:55 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 01:06:55 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 01:07:52 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 01:16:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 01:16:42 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 01:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 01:16:43 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 01:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:16:44 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 01:16:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a157c308d3669daf8d9e045739a35657c959a5ec42270b7147d4489ee10f57bf`  
		Last Modified: Thu, 12 Aug 2021 23:27:08 GMT  
		Size: 24.2 MB (24151515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdb4bcbb171cbfba72bf8c9715d36edf3949bc8dc58f0e83e835e99ee6a76a3`  
		Last Modified: Thu, 12 Aug 2021 23:26:57 GMT  
		Size: 2.4 MB (2414811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcb2a9161ac2664fc2799ef578a6d193532a670b49414c2fd3920169aa18ba1`  
		Last Modified: Thu, 12 Aug 2021 23:26:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0468520d35faf2e3e34ca95fb3a0b921b9bf74cba5d8e21603c607aad6e6056d`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 9.9 KB (9910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ebfec40337bb10a4a113a5fa394d707e40afa4d54c7834e1b40368c03c8d4b`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 734.0 KB (734013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22f58fb5a660e7280c5c97ac548346933c7d4cab498c786f416d8319635b82d`  
		Last Modified: Fri, 13 Aug 2021 01:17:25 GMT  
		Size: 9.4 MB (9402981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc1231a993aa0298932d54d3487d0e00eea8be3ccb53dd1ec3044df46532a8d`  
		Last Modified: Fri, 13 Aug 2021 01:17:59 GMT  
		Size: 55.5 MB (55536419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243eef57344af5e93f724b40a63171e67c28e5292ab843668e43254a4195bde0`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fccd4feeebf38924f9dbbe08f7d9dd82da67b15c655a65c4b4a134ee10a9a910
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93653630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02a65e5f462767393e652e046387d4213160fb29d7dae0fd51582c4b4ffe052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:56 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Fri, 30 Jul 2021 18:36:57 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 23:19:34 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 23:34:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 23:34:12 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:34:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 23:34:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:34:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:34:21 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 08:45:17 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 08:45:18 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:45:18 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:46:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:46:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:46:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:46:02 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 08:52:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:52:37 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:52:38 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:52:39 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 08:52:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:52:40 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:52:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf136fe6d43db6833f192cab959dd15d2f7ddbd0deb165dbdcf164a1e30df6d`  
		Last Modified: Fri, 13 Aug 2021 00:38:24 GMT  
		Size: 23.7 MB (23708770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a0d668d5c0fecdf6b296d8a6421807cdcaca95f5008271f8ca9d4f25bfd375`  
		Last Modified: Fri, 13 Aug 2021 00:38:08 GMT  
		Size: 2.4 MB (2414693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e162f772f745614305f4ebc6502e61a9dc2bc332144089c3859b36ed24d0487c`  
		Last Modified: Fri, 13 Aug 2021 00:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868398bdc7dd230f3b41eeef84ffe2cdd3eeae867ac01cd345f3ffcb5d9e58db`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2912e9ad030da2a4a90ded28890da15a15d533a041f54c3214571ad6c543b90`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 671.2 KB (671157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd305150da8018a30dabd946fda884c2d2c7f232a01d63d5b0f2475323fb617e`  
		Last Modified: Fri, 13 Aug 2021 08:56:47 GMT  
		Size: 9.4 MB (9403084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c55fb0ce4a71e1354b788b62e1cf5ebe89390a1645236e76dc1099ec4ff05f`  
		Last Modified: Fri, 13 Aug 2021 08:57:46 GMT  
		Size: 55.0 MB (55036232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d255b5196cf6763d0f55dc3dfff03d871e25f64e622c930dbe7be01372008f8`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:844f5c1fcec21acc4f9891ae694f2aac3e619a87ea513474850c5bdc619d27ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95916780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf2953a4f56170338349821197f830071b868242b2917f9ff98a8839a04b9d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:09 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Tue, 15 Jun 2021 21:45:09 GMT
CMD ["/bin/sh"]
# Fri, 13 Aug 2021 01:05:30 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 01:33:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 13 Aug 2021 01:33:37 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 01:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 13 Aug 2021 01:33:43 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 01:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:33:43 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:31:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 05:31:25 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 05:31:25 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:31:25 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:31:48 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:31:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:31:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:31:49 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 05:35:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:35:11 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:35:11 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:35:12 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 05:35:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:35:12 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:35:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c2a5a7092796a92bc42dbed25df2fe05d1e688d8777a5cb4a4463b646f763`  
		Last Modified: Fri, 13 Aug 2021 02:54:43 GMT  
		Size: 24.9 MB (24862053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1296cae68381255931426d96056970c6b17fccbf21bda80ae111106644991b`  
		Last Modified: Fri, 13 Aug 2021 02:54:38 GMT  
		Size: 2.4 MB (2422807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b682014b2cab613154da9269d19af8de7f13125eee5238ec37c80f570f85b`  
		Last Modified: Fri, 13 Aug 2021 02:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ba7ef4dcef81729897900511a18d8ddcd89252fc6b5d22c5fd9dc3d9875662`  
		Last Modified: Fri, 13 Aug 2021 05:36:48 GMT  
		Size: 10.0 KB (10005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91f29270c709a271ba1feab49ffbed6f8c7ae2bdbb47bf463e4ea249e2e435`  
		Last Modified: Fri, 13 Aug 2021 05:36:49 GMT  
		Size: 791.7 KB (791704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f3cd29637fc6b40d14e28bc72dbdf1646e06806a14eb2abf6268e8aa2e4e14`  
		Last Modified: Fri, 13 Aug 2021 05:36:51 GMT  
		Size: 9.4 MB (9403256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee00df371012cfdfc6d7931e01971c404c3f916dfe3d836472e7bc9e7c9cd1`  
		Last Modified: Fri, 13 Aug 2021 05:37:03 GMT  
		Size: 55.7 MB (55715436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e4513517425e2ebf602f7e0cf95689611376d483f289abb0278654e213f9`  
		Last Modified: Fri, 13 Aug 2021 05:36:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:3.42.5`

```console
$ docker pull ghost@sha256:3458dd98a6b39da644741713993c26ddef0add1a175408b4e5688113536b4882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:3.42.5` - linux; amd64

```console
$ docker pull ghost@sha256:cf569e68b046c86bd1489cf7590e1fce2abc172b52ffd308b1630d51d5abeadb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134596069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2018be159de67b6c3e8255e1668f0a99ad25660114c6d3830a3b21dfecdf99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:29:34 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 18:29:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:29:59 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:30:13 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:30:13 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:30:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:30:13 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:05:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:05:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:05:49 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:05:49 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:06:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:06:13 GMT
ENV GHOST_VERSION=3.42.5
# Thu, 12 Aug 2021 19:07:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:07:26 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:07:26 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:07:26 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:07:27 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:07:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898470a632a79ae16e4ea22c47f9e9975540952b925f81c1ba43f03b85e8664b`  
		Last Modified: Thu, 12 Aug 2021 18:44:24 GMT  
		Size: 24.1 MB (24085481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8450ead35388e1677754e1c319fd3f3462f6a8a647974f7218e5369157b254`  
		Last Modified: Thu, 12 Aug 2021 18:44:21 GMT  
		Size: 2.7 MB (2732673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fc3fe1c99886a85c41d2ba3fe143b30b347990fc8e164d10a4c91c52fa4858`  
		Last Modified: Thu, 12 Aug 2021 18:44:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957351c07eb33669ef5c578947c1b2fa8637657978f356004e61b78be9829370`  
		Last Modified: Thu, 12 Aug 2021 19:10:31 GMT  
		Size: 1.4 MB (1417769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7fcb63dedd0f683f805dad6b4749d8a9ccfacd079794728781456ebe5f3bd`  
		Last Modified: Thu, 12 Aug 2021 19:10:33 GMT  
		Size: 9.4 MB (9403232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b186d95582b7f2c202936c7e5fa087fc357dcd2f2b95fcf4b19822891ff0a0b`  
		Last Modified: Thu, 12 Aug 2021 19:10:44 GMT  
		Size: 69.8 MB (69806109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543acde8e5d7f1cc90b9344c17e4cf4692792049d68131988793b1c68ccc73e`  
		Last Modified: Thu, 12 Aug 2021 19:10:30 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6ae1da20c063947cced09004ccfdf852de5a0e57f95d3d46569af5a5209dc80e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130033887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd965cf8e32c6457235833195e846bb963ab3d266b33410ae27ce45094e2bcfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:07:00 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 00:07:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:07:51 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:08:25 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:08:26 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:08:27 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:36:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:36:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:36:47 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:36:47 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:37:29 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:37:30 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:37:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:37:31 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 08:44:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:44:59 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:45:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:45:00 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:45:01 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:45:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7db126ab438449a8bcf711971bc4deab9df4d3e95a63695935ee8ec9a5967c`  
		Last Modified: Fri, 13 Aug 2021 00:40:55 GMT  
		Size: 22.1 MB (22098693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c9a84de4e74befb623de090a65ff6587798ee25784d07a82c2576520609cf`  
		Last Modified: Fri, 13 Aug 2021 00:40:40 GMT  
		Size: 2.7 MB (2722750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09202bcb411b3332eafda7b1e253a93da633dee9af1918ae123e86f7e372d7`  
		Last Modified: Fri, 13 Aug 2021 00:40:38 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c37c446e44e9fba2c95433f4153d3e27ed5022dfcec70df7cb481851d5b640`  
		Last Modified: Fri, 13 Aug 2021 08:54:57 GMT  
		Size: 1.4 MB (1370027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1c9f1ee47bed50e701744b9c034a650eabfd6273d1176246cacf3fba1072ff`  
		Last Modified: Fri, 13 Aug 2021 08:55:11 GMT  
		Size: 9.4 MB (9403133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff40cf01a277693ae40fd1e12668ebc263eb6875b6fd527df8d9a293cb64220`  
		Last Modified: Fri, 13 Aug 2021 08:56:16 GMT  
		Size: 71.7 MB (71688300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7288fe54a2cdb9e7c3ca762225a2dd7f58da1461fbf371d17adf73301103eb`  
		Last Modified: Fri, 13 Aug 2021 08:54:56 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f8a6de2bfbb90af004ca6d6be620f90092cd64d8b741f10f4b6762622d9ac38d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118468898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36821ec35e7d84ae8bbe5070aa673b2e596c5b50fca2d5fbe7b33e02023a5e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 02:37:33 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 02:37:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 02:37:58 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 02:38:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 02:38:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 02:38:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 02:38:10 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:27:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:27:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:27:37 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:27:37 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:27:58 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:27:59 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 05:31:11 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:31:14 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:31:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:31:14 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:31:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:31:14 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:31:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26340cf10c1677ec31c5ee3b0cb08965c319b225b03cb003546875af641f2aab`  
		Last Modified: Fri, 13 Aug 2021 02:56:15 GMT  
		Size: 24.0 MB (24047327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eacc37cfc88d18feabbe269c22658aedadaab8db5ad63d0e2b6392c852d79fe`  
		Last Modified: Fri, 13 Aug 2021 02:56:11 GMT  
		Size: 2.7 MB (2732685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4520068f7780f46664f5ae4f99bfd975b1a95c54bab31a487065928720d707b`  
		Last Modified: Fri, 13 Aug 2021 02:56:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcb305ca7bd0c471e8000f7ff964f8ff31af8350b2259213ff081deb6557c9c`  
		Last Modified: Fri, 13 Aug 2021 05:36:19 GMT  
		Size: 1.4 MB (1353052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cabd63bd66d56211b3ade8b07afd3995f40a836d05b2cad627ac9dd1b4255`  
		Last Modified: Fri, 13 Aug 2021 05:36:21 GMT  
		Size: 9.4 MB (9403175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50513bee7d53d884f6aa3b08b7b7c599117d37b6ea6f4f939b1102967ab2acd`  
		Last Modified: Fri, 13 Aug 2021 05:36:33 GMT  
		Size: 55.0 MB (55012847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3112c9cda56f6b18bc7b6b5e2026d21583c7a8350a6cd5a229dd77fd4d66d`  
		Last Modified: Fri, 13 Aug 2021 05:36:18 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5` - linux; ppc64le

```console
$ docker pull ghost@sha256:635c4d7f12b1b639e9a16b1bd3b1eb1f5ce242777d2f2f6c09bd461ea869ad8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123925762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1647a15add09885e872de0f57aadd8d4d501c147ab3732de2aedc3e5b7bdcbdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:38:13 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 23:41:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:41:28 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:44:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:44:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:44:28 GMT
CMD ["node"]
# Fri, 13 Aug 2021 04:15:27 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 04:17:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 04:17:56 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 04:18:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 04:19:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 04:19:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 04:19:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 04:19:13 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 04:45:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:45:29 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:45:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:45:41 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991fe4a926e7cbbf8018cba4b4620c7ae60a970a1f21bcc5a14a0cf9172eaed2`  
		Last Modified: Fri, 13 Aug 2021 00:04:09 GMT  
		Size: 23.9 MB (23904766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1088ffa32997d36c1b61a835ad8a9ff25fa215d3969626a759983cdba4976aa8`  
		Last Modified: Fri, 13 Aug 2021 00:04:04 GMT  
		Size: 2.7 MB (2733492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fd362f0351dc1187856731938aaf1376e0288ed6f0b6bf0a689bdc69a6dbc2`  
		Last Modified: Fri, 13 Aug 2021 00:04:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fb97db4812d407e8d082e574b4e55c8d53822909f2fed45df638654529175`  
		Last Modified: Fri, 13 Aug 2021 04:49:05 GMT  
		Size: 1.3 MB (1338516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f3fa44e0632e353b5af610ba76f42482f2239af4f786212e06c066a2ad5e62`  
		Last Modified: Fri, 13 Aug 2021 04:50:25 GMT  
		Size: 9.4 MB (9403220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c734fbebb843a669e574d8a6e7bf0661a40a5f903f7e95a1bc05df75e618f56`  
		Last Modified: Fri, 13 Aug 2021 04:49:23 GMT  
		Size: 56.0 MB (55987035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55489146a622e3b3db972e92cd327a0f815a6d22deb9320407966cd3aed1c01d`  
		Last Modified: Fri, 13 Aug 2021 04:49:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5` - linux; s390x

```console
$ docker pull ghost@sha256:6e0ae8e0202abd874285b51d1ac7486c3f82d72be3effd9daf9f6e9eb877859b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118476122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720709dd6c6941fe6c538d8fd26597116bec6d8f5955521f104dc74e0b51d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:13:59 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 00:14:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:14:35 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:14:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:14:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:14:54 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:05:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:06:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:06:04 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:06:04 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:06:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:06:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:06:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:06:40 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 03:11:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:11:41 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:11:41 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:11:41 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:11:42 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:11:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3a7258908acb720d296cb0754dddac615f2876d0b9b422867f90c1cfb04df6`  
		Last Modified: Fri, 13 Aug 2021 00:23:39 GMT  
		Size: 24.2 MB (24169257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39fd2cf86fc931078497991d1c069a40f52c846758c59bd0aff46da81fd6485`  
		Last Modified: Fri, 13 Aug 2021 00:23:35 GMT  
		Size: 2.7 MB (2734985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80974528664444037f64e3df3b63d4183dd855fe96d5dbe4f5ce28c5acba1e4`  
		Last Modified: Fri, 13 Aug 2021 00:23:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59981678f3076807402eedf63786632a7b471f2660bb6b61198b9b75e73cb8b1`  
		Last Modified: Fri, 13 Aug 2021 03:12:34 GMT  
		Size: 1.4 MB (1404654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397f70381efd51568fa60e3b543288d48bf5f0954fb68d364f410d9ef1f9ca4c`  
		Last Modified: Fri, 13 Aug 2021 03:12:36 GMT  
		Size: 9.4 MB (9403244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09650d3f76c279b4a99c888df6115c0c13011f438e6b3e22957491a49f946f9`  
		Last Modified: Fri, 13 Aug 2021 03:12:45 GMT  
		Size: 55.0 MB (54998196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbe25f71607668d5a08a56504f56f102456b012981a92578aff198f9f123394`  
		Last Modified: Fri, 13 Aug 2021 03:12:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:3.42.5-alpine`

```console
$ docker pull ghost@sha256:3ef07877df2a81cf65f8b5a874584881d00da9fd9b797abc8eed4507d2006112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:3.42.5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1eb63fbf1b030f71441af606f13554e9268634d1955cf990f87fa864b1a250e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110904556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9113d247f1c3c3891f5b5e2cd683ecee3b5e3f6fbaf5febe71af74e9527ac67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:28:27 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 18:28:33 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:28:33 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:28:37 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:28:37 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:28:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:28:38 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:07:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:07:35 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:07:36 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:07:36 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:07:56 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:07:57 GMT
ENV GHOST_VERSION=3.42.5
# Thu, 12 Aug 2021 19:09:04 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:09:07 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:09:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:09:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:09:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:09:07 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:09:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13957d0e312b001d87caca22b0e000f8983402f248ef35e02a184dfcea7a1acb`  
		Last Modified: Thu, 12 Aug 2021 18:42:57 GMT  
		Size: 24.7 MB (24723955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755eebb143c1c9ba699653d6cac3cdbc450ecdcea90612024dcfc08d3c85587c`  
		Last Modified: Thu, 12 Aug 2021 18:42:53 GMT  
		Size: 2.4 MB (2362228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5af900a4f5080da3e57cab4aa7464c4e54f181266075ea05041c67df15e4c63`  
		Last Modified: Thu, 12 Aug 2021 18:42:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775ac215e323ecf0edfc6eaaa0b2620470b24b204f78925d20780c04dcc1e89d`  
		Last Modified: Thu, 12 Aug 2021 19:10:58 GMT  
		Size: 10.1 KB (10069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc2391737d2388dc2178fdd4745064be34a7b3761ee40b7729bbdc09ad847f`  
		Last Modified: Thu, 12 Aug 2021 19:10:59 GMT  
		Size: 779.6 KB (779644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93de3a2a20df8dedf2a3437161acbc2fa1298c85974c9ecee0475f45f496873`  
		Last Modified: Thu, 12 Aug 2021 19:11:01 GMT  
		Size: 9.4 MB (9403191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b081aea7dba6cb43149a4aea518302d8474b645a058ee68aa424ae4b3bd7bd4d`  
		Last Modified: Thu, 12 Aug 2021 19:11:13 GMT  
		Size: 70.8 MB (70824070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98e8d82f3a6e32e1009ca147b4dad078630da13d12227e04e090044351e495`  
		Last Modified: Thu, 12 Aug 2021 19:10:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:924d4776e85cbcefd409d2700a1b818d06ebfb551d6ccac31747d0a8d6c0f39e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94855730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518cf837a7a36e8908a40ce0a10c15853407fa9d280ff0027a571c2d007d616a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:06 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Fri, 30 Jul 2021 17:50:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 22:15:53 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 22:33:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 22:33:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:33:29 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 22:33:31 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:33:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:33:32 GMT
CMD ["node"]
# Fri, 13 Aug 2021 01:06:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 01:06:54 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 01:06:55 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 01:06:55 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 01:07:52 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 01:07:54 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 01:16:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 01:16:42 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 01:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 01:16:43 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 01:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:16:44 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 01:16:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a157c308d3669daf8d9e045739a35657c959a5ec42270b7147d4489ee10f57bf`  
		Last Modified: Thu, 12 Aug 2021 23:27:08 GMT  
		Size: 24.2 MB (24151515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdb4bcbb171cbfba72bf8c9715d36edf3949bc8dc58f0e83e835e99ee6a76a3`  
		Last Modified: Thu, 12 Aug 2021 23:26:57 GMT  
		Size: 2.4 MB (2414811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcb2a9161ac2664fc2799ef578a6d193532a670b49414c2fd3920169aa18ba1`  
		Last Modified: Thu, 12 Aug 2021 23:26:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0468520d35faf2e3e34ca95fb3a0b921b9bf74cba5d8e21603c607aad6e6056d`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 9.9 KB (9910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ebfec40337bb10a4a113a5fa394d707e40afa4d54c7834e1b40368c03c8d4b`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 734.0 KB (734013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22f58fb5a660e7280c5c97ac548346933c7d4cab498c786f416d8319635b82d`  
		Last Modified: Fri, 13 Aug 2021 01:17:25 GMT  
		Size: 9.4 MB (9402981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc1231a993aa0298932d54d3487d0e00eea8be3ccb53dd1ec3044df46532a8d`  
		Last Modified: Fri, 13 Aug 2021 01:17:59 GMT  
		Size: 55.5 MB (55536419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243eef57344af5e93f724b40a63171e67c28e5292ab843668e43254a4195bde0`  
		Last Modified: Fri, 13 Aug 2021 01:17:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fccd4feeebf38924f9dbbe08f7d9dd82da67b15c655a65c4b4a134ee10a9a910
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93653630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02a65e5f462767393e652e046387d4213160fb29d7dae0fd51582c4b4ffe052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:56 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Fri, 30 Jul 2021 18:36:57 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 23:19:34 GMT
ENV NODE_VERSION=12.22.5
# Thu, 12 Aug 2021 23:34:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 23:34:12 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:34:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 23:34:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:34:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:34:21 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 08:45:17 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 08:45:18 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:45:18 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:46:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:46:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:46:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:46:02 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 08:52:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:52:37 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:52:38 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:52:39 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 08:52:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:52:40 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:52:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf136fe6d43db6833f192cab959dd15d2f7ddbd0deb165dbdcf164a1e30df6d`  
		Last Modified: Fri, 13 Aug 2021 00:38:24 GMT  
		Size: 23.7 MB (23708770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a0d668d5c0fecdf6b296d8a6421807cdcaca95f5008271f8ca9d4f25bfd375`  
		Last Modified: Fri, 13 Aug 2021 00:38:08 GMT  
		Size: 2.4 MB (2414693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e162f772f745614305f4ebc6502e61a9dc2bc332144089c3859b36ed24d0487c`  
		Last Modified: Fri, 13 Aug 2021 00:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868398bdc7dd230f3b41eeef84ffe2cdd3eeae867ac01cd345f3ffcb5d9e58db`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2912e9ad030da2a4a90ded28890da15a15d533a041f54c3214571ad6c543b90`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 671.2 KB (671157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd305150da8018a30dabd946fda884c2d2c7f232a01d63d5b0f2475323fb617e`  
		Last Modified: Fri, 13 Aug 2021 08:56:47 GMT  
		Size: 9.4 MB (9403084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c55fb0ce4a71e1354b788b62e1cf5ebe89390a1645236e76dc1099ec4ff05f`  
		Last Modified: Fri, 13 Aug 2021 08:57:46 GMT  
		Size: 55.0 MB (55036232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d255b5196cf6763d0f55dc3dfff03d871e25f64e622c930dbe7be01372008f8`  
		Last Modified: Fri, 13 Aug 2021 08:56:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3.42.5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:844f5c1fcec21acc4f9891ae694f2aac3e619a87ea513474850c5bdc619d27ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95916780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf2953a4f56170338349821197f830071b868242b2917f9ff98a8839a04b9d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:09 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Tue, 15 Jun 2021 21:45:09 GMT
CMD ["/bin/sh"]
# Fri, 13 Aug 2021 01:05:30 GMT
ENV NODE_VERSION=12.22.5
# Fri, 13 Aug 2021 01:33:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="1c8ce0d58828faff84486dc116ec817595841c8578ed01266eb69e5383c73201"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Fri, 13 Aug 2021 01:33:37 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 01:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 13 Aug 2021 01:33:43 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 01:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:33:43 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:31:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 13 Aug 2021 05:31:25 GMT
RUN apk add --no-cache 		bash
# Fri, 13 Aug 2021 05:31:25 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:31:25 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:31:48 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:31:48 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:31:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:31:49 GMT
ENV GHOST_VERSION=3.42.5
# Fri, 13 Aug 2021 05:35:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:35:11 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:35:11 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:35:12 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 13 Aug 2021 05:35:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:35:12 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:35:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c2a5a7092796a92bc42dbed25df2fe05d1e688d8777a5cb4a4463b646f763`  
		Last Modified: Fri, 13 Aug 2021 02:54:43 GMT  
		Size: 24.9 MB (24862053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1296cae68381255931426d96056970c6b17fccbf21bda80ae111106644991b`  
		Last Modified: Fri, 13 Aug 2021 02:54:38 GMT  
		Size: 2.4 MB (2422807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b682014b2cab613154da9269d19af8de7f13125eee5238ec37c80f570f85b`  
		Last Modified: Fri, 13 Aug 2021 02:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ba7ef4dcef81729897900511a18d8ddcd89252fc6b5d22c5fd9dc3d9875662`  
		Last Modified: Fri, 13 Aug 2021 05:36:48 GMT  
		Size: 10.0 KB (10005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91f29270c709a271ba1feab49ffbed6f8c7ae2bdbb47bf463e4ea249e2e435`  
		Last Modified: Fri, 13 Aug 2021 05:36:49 GMT  
		Size: 791.7 KB (791704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f3cd29637fc6b40d14e28bc72dbdf1646e06806a14eb2abf6268e8aa2e4e14`  
		Last Modified: Fri, 13 Aug 2021 05:36:51 GMT  
		Size: 9.4 MB (9403256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee00df371012cfdfc6d7931e01971c404c3f916dfe3d836472e7bc9e7c9cd1`  
		Last Modified: Fri, 13 Aug 2021 05:37:03 GMT  
		Size: 55.7 MB (55715436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e4513517425e2ebf602f7e0cf95689611376d483f289abb0278654e213f9`  
		Last Modified: Fri, 13 Aug 2021 05:36:48 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4`

```console
$ docker pull ghost@sha256:a2a54a31e876f2f6dbf877e100f6488b3ecd950f55d36db7d4c90406df952f58
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
$ docker pull ghost@sha256:73832c333cbc6cc70499cd418fdb84054318247585c24feaba26b636a889a89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134928781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64409a1c4e09d185e9991ffd22515ac44d08edd6c789a5c144e2e5e62a88116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:25:54 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:26:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:26:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:26:32 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:26:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:26:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:26:33 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:02:17 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:02:28 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:02:28 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:02:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:03:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:03:49 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:03:49 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:03:49 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:03:49 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:03:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909f9fda05d6eb8bf705ba9a4bf4f5a9c917b35633cf8eb74e6acdd595b7b054`  
		Last Modified: Thu, 12 Aug 2021 18:40:51 GMT  
		Size: 35.4 MB (35384577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af9fc99b7260cc710839b8ab78ff00033edbfe29871cfdc6d47b0db2199a03`  
		Last Modified: Thu, 12 Aug 2021 18:40:46 GMT  
		Size: 2.7 MB (2733336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2744d2cf1e2363ca14a2668dab2e624922118df879b2795a664b98c0c74bd552`  
		Last Modified: Thu, 12 Aug 2021 18:40:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1585356a07d753e5a1172fda08a844c54f560f0880e2ff2fb20dcb4f5e5b908a`  
		Last Modified: Thu, 12 Aug 2021 19:09:35 GMT  
		Size: 1.4 MB (1417770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fce8d334512b8d30cd79c3e7c6ccd6dd15d143a08f72c3a3e3ce3a16975d2e`  
		Last Modified: Thu, 12 Aug 2021 19:09:38 GMT  
		Size: 9.4 MB (9403169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43a097b6efef54d34ca942479780d32a49d4b0770696aca338d06ae2c1ac22b`  
		Last Modified: Thu, 12 Aug 2021 19:09:46 GMT  
		Size: 58.8 MB (58839124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556f6441c9fb8b1c854156a6dbfafcbeec02eb628c4a9a3a169f2d693d91d903`  
		Last Modified: Thu, 12 Aug 2021 19:09:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm variant v7

```console
$ docker pull ghost@sha256:702bbfdb54637f4bb91a4dde3f8bf806b7e95d75f48b99fe38bf08daa6ebb2df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134316149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24f7a976a14df375f69ed159f93a9698e11d8094c823e6d5fa469741d5a2d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:00:30 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 23:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:01:34 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:02:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:02:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:02:25 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:12:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:13:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:13:29 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:13:29 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:14:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:14:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 08:21:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:21:33 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:21:34 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:21:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:21:35 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:21:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3bee9b560c58119f2fccc5a525fe07200eef8667a40c7fc4ce9a68007910d`  
		Last Modified: Fri, 13 Aug 2021 00:34:27 GMT  
		Size: 33.6 MB (33583856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d03355f4f0372dc1670aef9caca21a1de39f8c5ee8ff491ed00efda264165f9`  
		Last Modified: Fri, 13 Aug 2021 00:34:05 GMT  
		Size: 2.7 MB (2723035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6c4286b40066330b2321f01cdee653967291daf08cc3121e074ed9d6f051ff`  
		Last Modified: Fri, 13 Aug 2021 00:34:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692a9bc10bd98e1bc165cb98d33655b0ebccd1c135940f07fe0f28b75d83dc2`  
		Last Modified: Fri, 13 Aug 2021 08:53:36 GMT  
		Size: 1.4 MB (1370087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093ecaf67abbbc6fea806afe9922f38ca72874754acfdddb8db5cd648bf27e33`  
		Last Modified: Fri, 13 Aug 2021 08:53:49 GMT  
		Size: 9.4 MB (9403366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b583d3a9e7b93879a892a08ea7c52572c3d2fa44446cf349f40a411631720f5`  
		Last Modified: Fri, 13 Aug 2021 08:54:34 GMT  
		Size: 64.5 MB (64484819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aea994c24b4db86f14e1c684022befb72c030cd2975e67f675398d0785cba0d`  
		Last Modified: Fri, 13 Aug 2021 08:53:35 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0946be565f4d6c5faac6bc4c9787d87acd422298c7cf46cafe60b507e9c3c859
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133232069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07775c88fc91a454477ce2947a9a7242d77e1f0140f6ffc79e601c2cfff35fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:34:34 GMT
ENV NODE_VERSION=14.17.5
# Fri, 13 Aug 2021 00:34:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:35:00 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:35:17 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:35:17 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:35:17 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:15:38 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:16:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:16:02 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:16:02 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:16:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:16:26 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 05:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:19:35 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:19:36 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:19:36 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f852c7ad0a132bc2311af4000aae71873bdaa05cb79e33ce6e90fbcb58c7c792`  
		Last Modified: Fri, 13 Aug 2021 02:52:14 GMT  
		Size: 35.5 MB (35500636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb2ca6c9cf2688290d19a82507ad79b3c48f0ced478879b25ef003b9701de4`  
		Last Modified: Fri, 13 Aug 2021 02:52:08 GMT  
		Size: 2.7 MB (2733181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6373680b3d9077dfd1a3e6e7d89797f48f77a3a0306dcc72be7622da027355fc`  
		Last Modified: Fri, 13 Aug 2021 02:52:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ca739efd0ac0d79e8ddf7a0ce7379b7d90d881439501658c836620eefe82c`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 1.4 MB (1353087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2d192a41d98b86f0d6ccde6896569f891eb39a7fd9a480882a439ccaf04c48`  
		Last Modified: Fri, 13 Aug 2021 05:35:49 GMT  
		Size: 9.4 MB (9403397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88ca1e8a30bed4ea6d000e0fe4766c9dba5497910593aa5f7989cd2c9fe115d`  
		Last Modified: Fri, 13 Aug 2021 05:36:00 GMT  
		Size: 58.3 MB (58321953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed45096bb3714dbea9fa1f475bc9be52f6357c87c94110aa336e865636c40b0d`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; ppc64le

```console
$ docker pull ghost@sha256:641d5468b043638f2e85eee8f692f15b6052d4be38a5bf101839417906d8cc6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7568b69fe7bb516732ad18fbaac029f4d0e7c7beadfb19465e2f1a36a2d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:07:56 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:13:31 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:17:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:17:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:17:50 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:42:29 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:44:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:44:58 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:45:08 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:46:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:47:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:47:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:47:11 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 04:14:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:14:57 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:15:02 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:15:10 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:15:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700700ba2d5aa928042009517157d005113c5294d9955507dda41cee2208ec0`  
		Last Modified: Fri, 13 Aug 2021 00:01:16 GMT  
		Size: 37.3 MB (37290566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150545c38e67102af6dbfae496efb15bbcc63e022d2c0874ad097a50bf8174c2`  
		Last Modified: Fri, 13 Aug 2021 00:00:19 GMT  
		Size: 2.7 MB (2734176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cac311421ba89abfb0ad0936386b31a47f151ad1db601b54f5b8769e8c96f4`  
		Last Modified: Fri, 13 Aug 2021 00:00:18 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcc999bcbd77fb0870285ab4e8bd86626d86f0d8a9d452d50a89f4fcc7f5dc6`  
		Last Modified: Fri, 13 Aug 2021 04:46:22 GMT  
		Size: 1.3 MB (1338766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7feaaaf058e300baaa0b9c338c1a6c6b13945d8014805af9d4f38dc5a7cc69`  
		Last Modified: Fri, 13 Aug 2021 04:47:43 GMT  
		Size: 9.4 MB (9403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3110289d82b47fbc91a92a5b43dea938fad2c5f72f21ea1442420692e99d414`  
		Last Modified: Fri, 13 Aug 2021 04:48:46 GMT  
		Size: 59.8 MB (59763172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296655aad5db71b12e50630876096352650e0da37f79912bbaa68cb49c432f28`  
		Last Modified: Fri, 13 Aug 2021 04:46:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4` - linux; s390x

```console
$ docker pull ghost@sha256:84cab829540ac78b1482e011037a87a49aa4a9bdfb020339c86c465234c9fa9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133832121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c30070a4db8effe061a38e325de3ca0eeec2fce6413948c11e8f9730b1eecc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:58:33 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:59:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:59:03 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:59:19 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:59:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:59:20 GMT
CMD ["node"]
# Fri, 13 Aug 2021 02:58:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 02:58:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 02:58:43 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 02:58:43 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 02:59:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 02:59:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 03:05:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:05:31 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:05:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:05:32 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:05:33 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:05:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52586f67f92f8b93c0e5a326fbba79b340d9770d07e28e36bf13901ae445205`  
		Last Modified: Fri, 13 Aug 2021 00:22:08 GMT  
		Size: 35.3 MB (35261198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31332acb30d45a9c3946e3f1b33141bb5a7210cbf9e47468ffc322bc187f53`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 2.7 MB (2734870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477a2e9f332d95dc46a743f115fcda854c78487acdbce98af315b2844f170b`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e35573df8a50fce6e878e4d1ea1d3f6163644023eb3092484069802b96eacb`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 1.4 MB (1404613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a165afdcafe23870ba965f4ceff95f436b153a706db5f448b895693dbdf555b0`  
		Last Modified: Fri, 13 Aug 2021 03:12:12 GMT  
		Size: 9.4 MB (9403269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c4d1b5e54d963852f6f5a21a14ce9d46301f11d38d8064e071f29fc97dce3`  
		Last Modified: Fri, 13 Aug 2021 03:12:21 GMT  
		Size: 59.3 MB (59262383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332145ac6b77a8d7c747fbada3da2a07fa8b4b832b8f4fe5881887bbe4e46f97`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4-alpine`

```console
$ docker pull ghost@sha256:10be3a72fc15b407c77b3b0011500a36521f0c5e35dfba4e722bd784fc98ee64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:fa9a0b227557c1bd67256c57d0064687eae342dbd8c9dbbc8c241ef2e954841d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e20cd3188cd667f5f8d712f0048e121b68497a4dcd134c6b4b3a5065eb4a7f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:24:52 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:25:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8889a3ea0d0d8247132cf257ccd4828ddcd7e373f67c875878035b131e9fa1ac"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:25:01 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:25:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:25:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:25:06 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:03:58 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:04:00 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:04:00 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:04:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:04:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:04:24 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:05:20 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:05:21 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:05:21 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:05:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:05:22 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:05:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be041776d41473f040fb8b924aa86e51d972f719f11d7cfbcde03e854c29873b`  
		Last Modified: Thu, 12 Aug 2021 18:39:39 GMT  
		Size: 36.4 MB (36376161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7121a0c5ed3697d8aca8b0a5f13e54f1b625879204319b26a806df9323348aeb`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 2.4 MB (2363494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01167fb2fbb67ec936b91ed3a483cecdc82bdd9ba7404a99f3cf989fc9d534bc`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89119b529b78e9f8ea0abb09a69188298f7a3f67836c016b5ef8351d27a9b2e9`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 10.4 KB (10445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9825b5f70cd025fce6f73990c9ec93b1160b1fdf3cd43fc9f12747cacfd60a`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 815.4 KB (815396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc31023b4063c72862f88a7122b4563c652b4094ec2a436b44a51a1fc563b0`  
		Last Modified: Thu, 12 Aug 2021 19:10:06 GMT  
		Size: 9.4 MB (9403273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd8ae57e04d2d88bade41d8ae38e3944948ddfe730d43df52aa0e86e73fded`  
		Last Modified: Thu, 12 Aug 2021 19:10:14 GMT  
		Size: 60.1 MB (60127803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f5d2f7ef001540101e76c9bae6be27f3b807500b1fbb06c136c0b6cff3a0ac`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2c2b960e32cbab5e1f998861460e292f077546616a4b71fb17bd83b9cb11ee99
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105709573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7338c3022b31079f288daad2f0d92edd6bffffc4c6348d630f1ae1eda503c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:55:26 GMT
ENV NODE_VERSION=14.16.1
# Thu, 15 Apr 2021 00:05:38 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="39fbbd09668472f1105bdb5a7c20675bd91649543d2bc25b6edc1293835661f1"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 00:05:49 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 00:06:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 00:06:40 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:06:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:06:51 GMT
CMD ["node"]
# Thu, 15 Apr 2021 06:40:28 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 06:40:32 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 06:40:33 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 06:40:34 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 06:42:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 06:42:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 06:42:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 19 Apr 2021 18:51:06 GMT
ENV GHOST_VERSION=4.2.2
# Mon, 19 Apr 2021 19:00:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 19 Apr 2021 19:01:06 GMT
WORKDIR /var/lib/ghost
# Mon, 19 Apr 2021 19:01:08 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 19 Apr 2021 19:01:11 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 19 Apr 2021 19:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 19:01:16 GMT
EXPOSE 2368
# Mon, 19 Apr 2021 19:01:18 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d613d1bd988cf91f887a0f175713490c7ecbf3723e56448e14c094d0e6ab5e`  
		Last Modified: Thu, 15 Apr 2021 01:04:18 GMT  
		Size: 35.3 MB (35282050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581328e4eab02d7443dd01ecaf06977fc06fc1db420b724b44f0a701f3888950`  
		Last Modified: Thu, 15 Apr 2021 01:04:01 GMT  
		Size: 2.4 MB (2418994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6817eedde9b1d89a661a6c8cdb790b185d1e4265640eb20ec09e50bf73aef1ad`  
		Last Modified: Thu, 15 Apr 2021 01:04:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c347f4642df1accad140860b76413076ba67afa20193df808bdcbbb0ca75aab`  
		Last Modified: Thu, 15 Apr 2021 07:08:26 GMT  
		Size: 10.2 KB (10169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee664d99f2ece4cd62f48f918d1608b19a87bd18ab812d33be858415a9ee2b7`  
		Last Modified: Thu, 15 Apr 2021 07:08:26 GMT  
		Size: 770.0 KB (770034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f052dfa090b3d64867a090af46ecd180017d11460e615197dddfd16987fcd5d9`  
		Last Modified: Thu, 15 Apr 2021 07:08:31 GMT  
		Size: 7.4 MB (7405801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e946f06d29fb6a7259e49c3533469e1e75a40f7a3ac2cac72f6a400671be594d`  
		Last Modified: Mon, 19 Apr 2021 19:12:31 GMT  
		Size: 57.2 MB (57199568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8295dd57e24cc3b28157e4805558024f403a9e2de7f7fc140cf52ca124990f8b`  
		Last Modified: Mon, 19 Apr 2021 19:11:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4dbd6b3fbdc7d52d4cf0a14af66f8a57fafc2871253c1f586651113e197a6ed3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104511451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999471521ac3c74a3e72da4379c0d982f57ad055b5e0ce8503f65a8671c60d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:05:34 GMT
ENV NODE_VERSION=14.16.1
# Thu, 15 Apr 2021 01:15:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="39fbbd09668472f1105bdb5a7c20675bd91649543d2bc25b6edc1293835661f1"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 01:15:05 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 01:15:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 01:15:14 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 01:15:17 GMT
CMD ["node"]
# Thu, 15 Apr 2021 07:41:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 07:42:00 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 07:42:01 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 07:42:02 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 07:42:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 07:42:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 07:42:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 19 Apr 2021 19:13:56 GMT
ENV GHOST_VERSION=4.2.2
# Mon, 19 Apr 2021 19:21:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 19 Apr 2021 19:21:14 GMT
WORKDIR /var/lib/ghost
# Mon, 19 Apr 2021 19:21:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 19 Apr 2021 19:21:16 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 19 Apr 2021 19:21:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 19:21:18 GMT
EXPOSE 2368
# Mon, 19 Apr 2021 19:21:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c6d3ab5692397f4b3dda95b1baaabed77836f07cef0f68074ae626cb5fa4d`  
		Last Modified: Thu, 15 Apr 2021 02:04:28 GMT  
		Size: 34.8 MB (34845688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a285b9fc74e98c71f8913e67fca20895f3d28821a908e59e28b4721ac02e834c`  
		Last Modified: Thu, 15 Apr 2021 02:04:17 GMT  
		Size: 2.4 MB (2419021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6472fff65d9a1f977f0e65377ee05c476ed275dbb87420579f4350e77b7436d6`  
		Last Modified: Thu, 15 Apr 2021 02:04:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe75d9806a08fa875e7689c05018ad9f092e409344e90f291d50572bfe1270e`  
		Last Modified: Thu, 15 Apr 2021 08:03:09 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529c989854591686d4e268dbab35e5f2a9474dd36c99d8aafb102357113327e4`  
		Last Modified: Thu, 15 Apr 2021 08:03:09 GMT  
		Size: 702.7 KB (702711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0430d16567b2579bc64ec55ddfda049fcf412c31ab546a9f59ae4e749b0c85ff`  
		Last Modified: Thu, 15 Apr 2021 08:03:13 GMT  
		Size: 7.4 MB (7405660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b2c4dbab78c78a8edc8485d35eeced7ec3ebc60c9aacc8a65afb7a0c8d1086`  
		Last Modified: Mon, 19 Apr 2021 19:38:52 GMT  
		Size: 56.7 MB (56703434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc8fc0841fac2e3d4c56f260ce8991c320625623376651447ff9654049b26fe`  
		Last Modified: Mon, 19 Apr 2021 19:38:20 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:eaf658adc70df6381f16e5693d75ce2829a657af462a1d89cf0787c8ca6489fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106855689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f17cf224c1c91725ad725c5908f337cbb419997c98d997d38795f5eb1207f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:24:28 GMT
ENV NODE_VERSION=14.16.1
# Thu, 15 Apr 2021 03:34:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="39fbbd09668472f1105bdb5a7c20675bd91649543d2bc25b6edc1293835661f1"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 03:34:54 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 03:34:59 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 03:35:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:35:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:35:03 GMT
CMD ["node"]
# Thu, 15 Apr 2021 10:36:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 10:36:06 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 10:36:07 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 10:36:07 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 10:36:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 10:36:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 10:36:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 19 Apr 2021 18:59:37 GMT
ENV GHOST_VERSION=4.2.2
# Mon, 19 Apr 2021 19:06:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 19 Apr 2021 19:06:41 GMT
WORKDIR /var/lib/ghost
# Mon, 19 Apr 2021 19:06:42 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 19 Apr 2021 19:06:43 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 19 Apr 2021 19:06:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 19:06:46 GMT
EXPOSE 2368
# Mon, 19 Apr 2021 19:06:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729b33cc95bff6a339d4894936440783f6d9f9b8fcff4f656804b5f51589e099`  
		Last Modified: Thu, 15 Apr 2021 04:26:11 GMT  
		Size: 36.1 MB (36069717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feadca8c3a3527e0f48c1607c14fad7086d1e389d648d007630e05e45bf296e9`  
		Last Modified: Thu, 15 Apr 2021 04:26:02 GMT  
		Size: 2.4 MB (2426507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed996482c38503f3989d457afabe2ff764c91f3a77eecf87396d7bf2cbd823ea`  
		Last Modified: Thu, 15 Apr 2021 04:26:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f75128272534058e6663ae62a83359fd62898780ba3037f72aedf9f76837a57`  
		Last Modified: Thu, 15 Apr 2021 10:56:01 GMT  
		Size: 10.3 KB (10326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715f63a2d909696a7b5221e74df9a4f5bab12aeb033d200bdbf4d2ecd5514162`  
		Last Modified: Thu, 15 Apr 2021 10:56:03 GMT  
		Size: 824.6 KB (824615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ce871bf143aa2d55af399248e4579cda2eeb9e5870ccd3a613abec404743ee`  
		Last Modified: Thu, 15 Apr 2021 10:56:13 GMT  
		Size: 7.4 MB (7405414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7e8ec1e337ee4774cdbdda0efb41b656aacd27cbadda350c13bfb2cd4ecec`  
		Last Modified: Mon, 19 Apr 2021 19:26:37 GMT  
		Size: 57.4 MB (57406254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6443a67e5f2e7324afd6ed765bb5bcf85a090926684cf6a533ebce3a4a1ab5`  
		Last Modified: Mon, 19 Apr 2021 19:26:06 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.11`

```console
$ docker pull ghost@sha256:a2a54a31e876f2f6dbf877e100f6488b3ecd950f55d36db7d4c90406df952f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.11` - linux; amd64

```console
$ docker pull ghost@sha256:73832c333cbc6cc70499cd418fdb84054318247585c24feaba26b636a889a89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134928781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64409a1c4e09d185e9991ffd22515ac44d08edd6c789a5c144e2e5e62a88116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:25:54 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:26:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:26:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:26:32 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:26:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:26:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:26:33 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:02:17 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:02:28 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:02:28 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:02:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:03:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:03:49 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:03:49 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:03:49 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:03:49 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:03:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909f9fda05d6eb8bf705ba9a4bf4f5a9c917b35633cf8eb74e6acdd595b7b054`  
		Last Modified: Thu, 12 Aug 2021 18:40:51 GMT  
		Size: 35.4 MB (35384577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af9fc99b7260cc710839b8ab78ff00033edbfe29871cfdc6d47b0db2199a03`  
		Last Modified: Thu, 12 Aug 2021 18:40:46 GMT  
		Size: 2.7 MB (2733336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2744d2cf1e2363ca14a2668dab2e624922118df879b2795a664b98c0c74bd552`  
		Last Modified: Thu, 12 Aug 2021 18:40:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1585356a07d753e5a1172fda08a844c54f560f0880e2ff2fb20dcb4f5e5b908a`  
		Last Modified: Thu, 12 Aug 2021 19:09:35 GMT  
		Size: 1.4 MB (1417770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fce8d334512b8d30cd79c3e7c6ccd6dd15d143a08f72c3a3e3ce3a16975d2e`  
		Last Modified: Thu, 12 Aug 2021 19:09:38 GMT  
		Size: 9.4 MB (9403169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43a097b6efef54d34ca942479780d32a49d4b0770696aca338d06ae2c1ac22b`  
		Last Modified: Thu, 12 Aug 2021 19:09:46 GMT  
		Size: 58.8 MB (58839124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556f6441c9fb8b1c854156a6dbfafcbeec02eb628c4a9a3a169f2d693d91d903`  
		Last Modified: Thu, 12 Aug 2021 19:09:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11` - linux; arm variant v7

```console
$ docker pull ghost@sha256:702bbfdb54637f4bb91a4dde3f8bf806b7e95d75f48b99fe38bf08daa6ebb2df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134316149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24f7a976a14df375f69ed159f93a9698e11d8094c823e6d5fa469741d5a2d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:00:30 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 23:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:01:34 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:02:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:02:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:02:25 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:12:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:13:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:13:29 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:13:29 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:14:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:14:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 08:21:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:21:33 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:21:34 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:21:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:21:35 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:21:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3bee9b560c58119f2fccc5a525fe07200eef8667a40c7fc4ce9a68007910d`  
		Last Modified: Fri, 13 Aug 2021 00:34:27 GMT  
		Size: 33.6 MB (33583856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d03355f4f0372dc1670aef9caca21a1de39f8c5ee8ff491ed00efda264165f9`  
		Last Modified: Fri, 13 Aug 2021 00:34:05 GMT  
		Size: 2.7 MB (2723035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6c4286b40066330b2321f01cdee653967291daf08cc3121e074ed9d6f051ff`  
		Last Modified: Fri, 13 Aug 2021 00:34:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692a9bc10bd98e1bc165cb98d33655b0ebccd1c135940f07fe0f28b75d83dc2`  
		Last Modified: Fri, 13 Aug 2021 08:53:36 GMT  
		Size: 1.4 MB (1370087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093ecaf67abbbc6fea806afe9922f38ca72874754acfdddb8db5cd648bf27e33`  
		Last Modified: Fri, 13 Aug 2021 08:53:49 GMT  
		Size: 9.4 MB (9403366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b583d3a9e7b93879a892a08ea7c52572c3d2fa44446cf349f40a411631720f5`  
		Last Modified: Fri, 13 Aug 2021 08:54:34 GMT  
		Size: 64.5 MB (64484819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aea994c24b4db86f14e1c684022befb72c030cd2975e67f675398d0785cba0d`  
		Last Modified: Fri, 13 Aug 2021 08:53:35 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0946be565f4d6c5faac6bc4c9787d87acd422298c7cf46cafe60b507e9c3c859
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133232069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07775c88fc91a454477ce2947a9a7242d77e1f0140f6ffc79e601c2cfff35fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:34:34 GMT
ENV NODE_VERSION=14.17.5
# Fri, 13 Aug 2021 00:34:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:35:00 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:35:17 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:35:17 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:35:17 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:15:38 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:16:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:16:02 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:16:02 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:16:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:16:26 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 05:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:19:35 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:19:36 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:19:36 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f852c7ad0a132bc2311af4000aae71873bdaa05cb79e33ce6e90fbcb58c7c792`  
		Last Modified: Fri, 13 Aug 2021 02:52:14 GMT  
		Size: 35.5 MB (35500636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb2ca6c9cf2688290d19a82507ad79b3c48f0ced478879b25ef003b9701de4`  
		Last Modified: Fri, 13 Aug 2021 02:52:08 GMT  
		Size: 2.7 MB (2733181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6373680b3d9077dfd1a3e6e7d89797f48f77a3a0306dcc72be7622da027355fc`  
		Last Modified: Fri, 13 Aug 2021 02:52:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ca739efd0ac0d79e8ddf7a0ce7379b7d90d881439501658c836620eefe82c`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 1.4 MB (1353087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2d192a41d98b86f0d6ccde6896569f891eb39a7fd9a480882a439ccaf04c48`  
		Last Modified: Fri, 13 Aug 2021 05:35:49 GMT  
		Size: 9.4 MB (9403397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88ca1e8a30bed4ea6d000e0fe4766c9dba5497910593aa5f7989cd2c9fe115d`  
		Last Modified: Fri, 13 Aug 2021 05:36:00 GMT  
		Size: 58.3 MB (58321953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed45096bb3714dbea9fa1f475bc9be52f6357c87c94110aa336e865636c40b0d`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11` - linux; ppc64le

```console
$ docker pull ghost@sha256:641d5468b043638f2e85eee8f692f15b6052d4be38a5bf101839417906d8cc6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7568b69fe7bb516732ad18fbaac029f4d0e7c7beadfb19465e2f1a36a2d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:07:56 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:13:31 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:17:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:17:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:17:50 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:42:29 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:44:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:44:58 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:45:08 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:46:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:47:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:47:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:47:11 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 04:14:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:14:57 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:15:02 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:15:10 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:15:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700700ba2d5aa928042009517157d005113c5294d9955507dda41cee2208ec0`  
		Last Modified: Fri, 13 Aug 2021 00:01:16 GMT  
		Size: 37.3 MB (37290566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150545c38e67102af6dbfae496efb15bbcc63e022d2c0874ad097a50bf8174c2`  
		Last Modified: Fri, 13 Aug 2021 00:00:19 GMT  
		Size: 2.7 MB (2734176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cac311421ba89abfb0ad0936386b31a47f151ad1db601b54f5b8769e8c96f4`  
		Last Modified: Fri, 13 Aug 2021 00:00:18 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcc999bcbd77fb0870285ab4e8bd86626d86f0d8a9d452d50a89f4fcc7f5dc6`  
		Last Modified: Fri, 13 Aug 2021 04:46:22 GMT  
		Size: 1.3 MB (1338766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7feaaaf058e300baaa0b9c338c1a6c6b13945d8014805af9d4f38dc5a7cc69`  
		Last Modified: Fri, 13 Aug 2021 04:47:43 GMT  
		Size: 9.4 MB (9403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3110289d82b47fbc91a92a5b43dea938fad2c5f72f21ea1442420692e99d414`  
		Last Modified: Fri, 13 Aug 2021 04:48:46 GMT  
		Size: 59.8 MB (59763172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296655aad5db71b12e50630876096352650e0da37f79912bbaa68cb49c432f28`  
		Last Modified: Fri, 13 Aug 2021 04:46:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11` - linux; s390x

```console
$ docker pull ghost@sha256:84cab829540ac78b1482e011037a87a49aa4a9bdfb020339c86c465234c9fa9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133832121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c30070a4db8effe061a38e325de3ca0eeec2fce6413948c11e8f9730b1eecc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:58:33 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:59:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:59:03 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:59:19 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:59:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:59:20 GMT
CMD ["node"]
# Fri, 13 Aug 2021 02:58:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 02:58:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 02:58:43 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 02:58:43 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 02:59:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 02:59:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 03:05:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:05:31 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:05:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:05:32 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:05:33 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:05:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52586f67f92f8b93c0e5a326fbba79b340d9770d07e28e36bf13901ae445205`  
		Last Modified: Fri, 13 Aug 2021 00:22:08 GMT  
		Size: 35.3 MB (35261198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31332acb30d45a9c3946e3f1b33141bb5a7210cbf9e47468ffc322bc187f53`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 2.7 MB (2734870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477a2e9f332d95dc46a743f115fcda854c78487acdbce98af315b2844f170b`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e35573df8a50fce6e878e4d1ea1d3f6163644023eb3092484069802b96eacb`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 1.4 MB (1404613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a165afdcafe23870ba965f4ceff95f436b153a706db5f448b895693dbdf555b0`  
		Last Modified: Fri, 13 Aug 2021 03:12:12 GMT  
		Size: 9.4 MB (9403269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c4d1b5e54d963852f6f5a21a14ce9d46301f11d38d8064e071f29fc97dce3`  
		Last Modified: Fri, 13 Aug 2021 03:12:21 GMT  
		Size: 59.3 MB (59262383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332145ac6b77a8d7c747fbada3da2a07fa8b4b832b8f4fe5881887bbe4e46f97`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.11-alpine`

```console
$ docker pull ghost@sha256:d24d7214a59b5b7aa4a48acaa716c04651cf428ec3ac96ffa2628562c43412eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ghost:4.11-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:fa9a0b227557c1bd67256c57d0064687eae342dbd8c9dbbc8c241ef2e954841d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e20cd3188cd667f5f8d712f0048e121b68497a4dcd134c6b4b3a5065eb4a7f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:24:52 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:25:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8889a3ea0d0d8247132cf257ccd4828ddcd7e373f67c875878035b131e9fa1ac"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:25:01 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:25:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:25:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:25:06 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:03:58 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:04:00 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:04:00 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:04:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:04:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:04:24 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:05:20 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:05:21 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:05:21 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:05:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:05:22 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:05:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be041776d41473f040fb8b924aa86e51d972f719f11d7cfbcde03e854c29873b`  
		Last Modified: Thu, 12 Aug 2021 18:39:39 GMT  
		Size: 36.4 MB (36376161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7121a0c5ed3697d8aca8b0a5f13e54f1b625879204319b26a806df9323348aeb`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 2.4 MB (2363494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01167fb2fbb67ec936b91ed3a483cecdc82bdd9ba7404a99f3cf989fc9d534bc`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89119b529b78e9f8ea0abb09a69188298f7a3f67836c016b5ef8351d27a9b2e9`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 10.4 KB (10445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9825b5f70cd025fce6f73990c9ec93b1160b1fdf3cd43fc9f12747cacfd60a`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 815.4 KB (815396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc31023b4063c72862f88a7122b4563c652b4094ec2a436b44a51a1fc563b0`  
		Last Modified: Thu, 12 Aug 2021 19:10:06 GMT  
		Size: 9.4 MB (9403273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd8ae57e04d2d88bade41d8ae38e3944948ddfe730d43df52aa0e86e73fded`  
		Last Modified: Thu, 12 Aug 2021 19:10:14 GMT  
		Size: 60.1 MB (60127803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f5d2f7ef001540101e76c9bae6be27f3b807500b1fbb06c136c0b6cff3a0ac`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.11.0`

```console
$ docker pull ghost@sha256:a2a54a31e876f2f6dbf877e100f6488b3ecd950f55d36db7d4c90406df952f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:4.11.0` - linux; amd64

```console
$ docker pull ghost@sha256:73832c333cbc6cc70499cd418fdb84054318247585c24feaba26b636a889a89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134928781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64409a1c4e09d185e9991ffd22515ac44d08edd6c789a5c144e2e5e62a88116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:25:54 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:26:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:26:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:26:32 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:26:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:26:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:26:33 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:02:17 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:02:28 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:02:28 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:02:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:03:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:03:49 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:03:49 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:03:49 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:03:49 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:03:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909f9fda05d6eb8bf705ba9a4bf4f5a9c917b35633cf8eb74e6acdd595b7b054`  
		Last Modified: Thu, 12 Aug 2021 18:40:51 GMT  
		Size: 35.4 MB (35384577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af9fc99b7260cc710839b8ab78ff00033edbfe29871cfdc6d47b0db2199a03`  
		Last Modified: Thu, 12 Aug 2021 18:40:46 GMT  
		Size: 2.7 MB (2733336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2744d2cf1e2363ca14a2668dab2e624922118df879b2795a664b98c0c74bd552`  
		Last Modified: Thu, 12 Aug 2021 18:40:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1585356a07d753e5a1172fda08a844c54f560f0880e2ff2fb20dcb4f5e5b908a`  
		Last Modified: Thu, 12 Aug 2021 19:09:35 GMT  
		Size: 1.4 MB (1417770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fce8d334512b8d30cd79c3e7c6ccd6dd15d143a08f72c3a3e3ce3a16975d2e`  
		Last Modified: Thu, 12 Aug 2021 19:09:38 GMT  
		Size: 9.4 MB (9403169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43a097b6efef54d34ca942479780d32a49d4b0770696aca338d06ae2c1ac22b`  
		Last Modified: Thu, 12 Aug 2021 19:09:46 GMT  
		Size: 58.8 MB (58839124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556f6441c9fb8b1c854156a6dbfafcbeec02eb628c4a9a3a169f2d693d91d903`  
		Last Modified: Thu, 12 Aug 2021 19:09:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:702bbfdb54637f4bb91a4dde3f8bf806b7e95d75f48b99fe38bf08daa6ebb2df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134316149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24f7a976a14df375f69ed159f93a9698e11d8094c823e6d5fa469741d5a2d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:00:30 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 23:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:01:34 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:02:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:02:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:02:25 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:12:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:13:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:13:29 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:13:29 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:14:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:14:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 08:21:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:21:33 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:21:34 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:21:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:21:35 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:21:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3bee9b560c58119f2fccc5a525fe07200eef8667a40c7fc4ce9a68007910d`  
		Last Modified: Fri, 13 Aug 2021 00:34:27 GMT  
		Size: 33.6 MB (33583856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d03355f4f0372dc1670aef9caca21a1de39f8c5ee8ff491ed00efda264165f9`  
		Last Modified: Fri, 13 Aug 2021 00:34:05 GMT  
		Size: 2.7 MB (2723035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6c4286b40066330b2321f01cdee653967291daf08cc3121e074ed9d6f051ff`  
		Last Modified: Fri, 13 Aug 2021 00:34:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692a9bc10bd98e1bc165cb98d33655b0ebccd1c135940f07fe0f28b75d83dc2`  
		Last Modified: Fri, 13 Aug 2021 08:53:36 GMT  
		Size: 1.4 MB (1370087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093ecaf67abbbc6fea806afe9922f38ca72874754acfdddb8db5cd648bf27e33`  
		Last Modified: Fri, 13 Aug 2021 08:53:49 GMT  
		Size: 9.4 MB (9403366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b583d3a9e7b93879a892a08ea7c52572c3d2fa44446cf349f40a411631720f5`  
		Last Modified: Fri, 13 Aug 2021 08:54:34 GMT  
		Size: 64.5 MB (64484819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aea994c24b4db86f14e1c684022befb72c030cd2975e67f675398d0785cba0d`  
		Last Modified: Fri, 13 Aug 2021 08:53:35 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0946be565f4d6c5faac6bc4c9787d87acd422298c7cf46cafe60b507e9c3c859
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133232069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07775c88fc91a454477ce2947a9a7242d77e1f0140f6ffc79e601c2cfff35fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:34:34 GMT
ENV NODE_VERSION=14.17.5
# Fri, 13 Aug 2021 00:34:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:35:00 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:35:17 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:35:17 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:35:17 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:15:38 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:16:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:16:02 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:16:02 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:16:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:16:26 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 05:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:19:35 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:19:36 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:19:36 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f852c7ad0a132bc2311af4000aae71873bdaa05cb79e33ce6e90fbcb58c7c792`  
		Last Modified: Fri, 13 Aug 2021 02:52:14 GMT  
		Size: 35.5 MB (35500636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb2ca6c9cf2688290d19a82507ad79b3c48f0ced478879b25ef003b9701de4`  
		Last Modified: Fri, 13 Aug 2021 02:52:08 GMT  
		Size: 2.7 MB (2733181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6373680b3d9077dfd1a3e6e7d89797f48f77a3a0306dcc72be7622da027355fc`  
		Last Modified: Fri, 13 Aug 2021 02:52:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ca739efd0ac0d79e8ddf7a0ce7379b7d90d881439501658c836620eefe82c`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 1.4 MB (1353087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2d192a41d98b86f0d6ccde6896569f891eb39a7fd9a480882a439ccaf04c48`  
		Last Modified: Fri, 13 Aug 2021 05:35:49 GMT  
		Size: 9.4 MB (9403397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88ca1e8a30bed4ea6d000e0fe4766c9dba5497910593aa5f7989cd2c9fe115d`  
		Last Modified: Fri, 13 Aug 2021 05:36:00 GMT  
		Size: 58.3 MB (58321953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed45096bb3714dbea9fa1f475bc9be52f6357c87c94110aa336e865636c40b0d`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:641d5468b043638f2e85eee8f692f15b6052d4be38a5bf101839417906d8cc6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7568b69fe7bb516732ad18fbaac029f4d0e7c7beadfb19465e2f1a36a2d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:07:56 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:13:31 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:17:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:17:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:17:50 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:42:29 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:44:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:44:58 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:45:08 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:46:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:47:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:47:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:47:11 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 04:14:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:14:57 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:15:02 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:15:10 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:15:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700700ba2d5aa928042009517157d005113c5294d9955507dda41cee2208ec0`  
		Last Modified: Fri, 13 Aug 2021 00:01:16 GMT  
		Size: 37.3 MB (37290566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150545c38e67102af6dbfae496efb15bbcc63e022d2c0874ad097a50bf8174c2`  
		Last Modified: Fri, 13 Aug 2021 00:00:19 GMT  
		Size: 2.7 MB (2734176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cac311421ba89abfb0ad0936386b31a47f151ad1db601b54f5b8769e8c96f4`  
		Last Modified: Fri, 13 Aug 2021 00:00:18 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcc999bcbd77fb0870285ab4e8bd86626d86f0d8a9d452d50a89f4fcc7f5dc6`  
		Last Modified: Fri, 13 Aug 2021 04:46:22 GMT  
		Size: 1.3 MB (1338766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7feaaaf058e300baaa0b9c338c1a6c6b13945d8014805af9d4f38dc5a7cc69`  
		Last Modified: Fri, 13 Aug 2021 04:47:43 GMT  
		Size: 9.4 MB (9403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3110289d82b47fbc91a92a5b43dea938fad2c5f72f21ea1442420692e99d414`  
		Last Modified: Fri, 13 Aug 2021 04:48:46 GMT  
		Size: 59.8 MB (59763172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296655aad5db71b12e50630876096352650e0da37f79912bbaa68cb49c432f28`  
		Last Modified: Fri, 13 Aug 2021 04:46:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4.11.0` - linux; s390x

```console
$ docker pull ghost@sha256:84cab829540ac78b1482e011037a87a49aa4a9bdfb020339c86c465234c9fa9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133832121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c30070a4db8effe061a38e325de3ca0eeec2fce6413948c11e8f9730b1eecc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:58:33 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:59:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:59:03 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:59:19 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:59:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:59:20 GMT
CMD ["node"]
# Fri, 13 Aug 2021 02:58:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 02:58:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 02:58:43 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 02:58:43 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 02:59:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 02:59:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 03:05:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:05:31 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:05:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:05:32 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:05:33 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:05:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52586f67f92f8b93c0e5a326fbba79b340d9770d07e28e36bf13901ae445205`  
		Last Modified: Fri, 13 Aug 2021 00:22:08 GMT  
		Size: 35.3 MB (35261198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31332acb30d45a9c3946e3f1b33141bb5a7210cbf9e47468ffc322bc187f53`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 2.7 MB (2734870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477a2e9f332d95dc46a743f115fcda854c78487acdbce98af315b2844f170b`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e35573df8a50fce6e878e4d1ea1d3f6163644023eb3092484069802b96eacb`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 1.4 MB (1404613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a165afdcafe23870ba965f4ceff95f436b153a706db5f448b895693dbdf555b0`  
		Last Modified: Fri, 13 Aug 2021 03:12:12 GMT  
		Size: 9.4 MB (9403269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c4d1b5e54d963852f6f5a21a14ce9d46301f11d38d8064e071f29fc97dce3`  
		Last Modified: Fri, 13 Aug 2021 03:12:21 GMT  
		Size: 59.3 MB (59262383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332145ac6b77a8d7c747fbada3da2a07fa8b4b832b8f4fe5881887bbe4e46f97`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:4.11.0-alpine`

```console
$ docker pull ghost@sha256:d24d7214a59b5b7aa4a48acaa716c04651cf428ec3ac96ffa2628562c43412eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ghost:4.11.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:fa9a0b227557c1bd67256c57d0064687eae342dbd8c9dbbc8c241ef2e954841d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e20cd3188cd667f5f8d712f0048e121b68497a4dcd134c6b4b3a5065eb4a7f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:24:52 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:25:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8889a3ea0d0d8247132cf257ccd4828ddcd7e373f67c875878035b131e9fa1ac"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:25:01 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:25:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:25:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:25:06 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:03:58 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:04:00 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:04:00 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:04:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:04:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:04:24 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:05:20 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:05:21 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:05:21 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:05:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:05:22 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:05:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be041776d41473f040fb8b924aa86e51d972f719f11d7cfbcde03e854c29873b`  
		Last Modified: Thu, 12 Aug 2021 18:39:39 GMT  
		Size: 36.4 MB (36376161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7121a0c5ed3697d8aca8b0a5f13e54f1b625879204319b26a806df9323348aeb`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 2.4 MB (2363494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01167fb2fbb67ec936b91ed3a483cecdc82bdd9ba7404a99f3cf989fc9d534bc`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89119b529b78e9f8ea0abb09a69188298f7a3f67836c016b5ef8351d27a9b2e9`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 10.4 KB (10445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9825b5f70cd025fce6f73990c9ec93b1160b1fdf3cd43fc9f12747cacfd60a`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 815.4 KB (815396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc31023b4063c72862f88a7122b4563c652b4094ec2a436b44a51a1fc563b0`  
		Last Modified: Thu, 12 Aug 2021 19:10:06 GMT  
		Size: 9.4 MB (9403273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd8ae57e04d2d88bade41d8ae38e3944948ddfe730d43df52aa0e86e73fded`  
		Last Modified: Thu, 12 Aug 2021 19:10:14 GMT  
		Size: 60.1 MB (60127803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f5d2f7ef001540101e76c9bae6be27f3b807500b1fbb06c136c0b6cff3a0ac`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:10be3a72fc15b407c77b3b0011500a36521f0c5e35dfba4e722bd784fc98ee64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:fa9a0b227557c1bd67256c57d0064687eae342dbd8c9dbbc8c241ef2e954841d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e20cd3188cd667f5f8d712f0048e121b68497a4dcd134c6b4b3a5065eb4a7f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 12 Aug 2021 18:24:52 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:25:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8889a3ea0d0d8247132cf257ccd4828ddcd7e373f67c875878035b131e9fa1ac"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 12 Aug 2021 18:25:01 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:25:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 12 Aug 2021 18:25:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:25:06 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:03:58 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 12 Aug 2021 19:04:00 GMT
RUN apk add --no-cache 		bash
# Thu, 12 Aug 2021 19:04:00 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:04:00 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:04:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:04:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:04:24 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:05:20 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:05:21 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:05:21 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:05:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 12 Aug 2021 19:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:05:22 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:05:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be041776d41473f040fb8b924aa86e51d972f719f11d7cfbcde03e854c29873b`  
		Last Modified: Thu, 12 Aug 2021 18:39:39 GMT  
		Size: 36.4 MB (36376161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7121a0c5ed3697d8aca8b0a5f13e54f1b625879204319b26a806df9323348aeb`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 2.4 MB (2363494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01167fb2fbb67ec936b91ed3a483cecdc82bdd9ba7404a99f3cf989fc9d534bc`  
		Last Modified: Thu, 12 Aug 2021 18:39:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89119b529b78e9f8ea0abb09a69188298f7a3f67836c016b5ef8351d27a9b2e9`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 10.4 KB (10445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9825b5f70cd025fce6f73990c9ec93b1160b1fdf3cd43fc9f12747cacfd60a`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 815.4 KB (815396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc31023b4063c72862f88a7122b4563c652b4094ec2a436b44a51a1fc563b0`  
		Last Modified: Thu, 12 Aug 2021 19:10:06 GMT  
		Size: 9.4 MB (9403273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd8ae57e04d2d88bade41d8ae38e3944948ddfe730d43df52aa0e86e73fded`  
		Last Modified: Thu, 12 Aug 2021 19:10:14 GMT  
		Size: 60.1 MB (60127803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f5d2f7ef001540101e76c9bae6be27f3b807500b1fbb06c136c0b6cff3a0ac`  
		Last Modified: Thu, 12 Aug 2021 19:10:03 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2c2b960e32cbab5e1f998861460e292f077546616a4b71fb17bd83b9cb11ee99
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105709573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7338c3022b31079f288daad2f0d92edd6bffffc4c6348d630f1ae1eda503c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:55:26 GMT
ENV NODE_VERSION=14.16.1
# Thu, 15 Apr 2021 00:05:38 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="39fbbd09668472f1105bdb5a7c20675bd91649543d2bc25b6edc1293835661f1"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 00:05:49 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 00:06:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 00:06:40 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:06:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:06:51 GMT
CMD ["node"]
# Thu, 15 Apr 2021 06:40:28 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 06:40:32 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 06:40:33 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 06:40:34 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 06:42:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 06:42:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 06:42:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 19 Apr 2021 18:51:06 GMT
ENV GHOST_VERSION=4.2.2
# Mon, 19 Apr 2021 19:00:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 19 Apr 2021 19:01:06 GMT
WORKDIR /var/lib/ghost
# Mon, 19 Apr 2021 19:01:08 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 19 Apr 2021 19:01:11 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 19 Apr 2021 19:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 19:01:16 GMT
EXPOSE 2368
# Mon, 19 Apr 2021 19:01:18 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d613d1bd988cf91f887a0f175713490c7ecbf3723e56448e14c094d0e6ab5e`  
		Last Modified: Thu, 15 Apr 2021 01:04:18 GMT  
		Size: 35.3 MB (35282050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581328e4eab02d7443dd01ecaf06977fc06fc1db420b724b44f0a701f3888950`  
		Last Modified: Thu, 15 Apr 2021 01:04:01 GMT  
		Size: 2.4 MB (2418994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6817eedde9b1d89a661a6c8cdb790b185d1e4265640eb20ec09e50bf73aef1ad`  
		Last Modified: Thu, 15 Apr 2021 01:04:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c347f4642df1accad140860b76413076ba67afa20193df808bdcbbb0ca75aab`  
		Last Modified: Thu, 15 Apr 2021 07:08:26 GMT  
		Size: 10.2 KB (10169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee664d99f2ece4cd62f48f918d1608b19a87bd18ab812d33be858415a9ee2b7`  
		Last Modified: Thu, 15 Apr 2021 07:08:26 GMT  
		Size: 770.0 KB (770034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f052dfa090b3d64867a090af46ecd180017d11460e615197dddfd16987fcd5d9`  
		Last Modified: Thu, 15 Apr 2021 07:08:31 GMT  
		Size: 7.4 MB (7405801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e946f06d29fb6a7259e49c3533469e1e75a40f7a3ac2cac72f6a400671be594d`  
		Last Modified: Mon, 19 Apr 2021 19:12:31 GMT  
		Size: 57.2 MB (57199568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8295dd57e24cc3b28157e4805558024f403a9e2de7f7fc140cf52ca124990f8b`  
		Last Modified: Mon, 19 Apr 2021 19:11:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4dbd6b3fbdc7d52d4cf0a14af66f8a57fafc2871253c1f586651113e197a6ed3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104511451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999471521ac3c74a3e72da4379c0d982f57ad055b5e0ce8503f65a8671c60d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:05:34 GMT
ENV NODE_VERSION=14.16.1
# Thu, 15 Apr 2021 01:15:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="39fbbd09668472f1105bdb5a7c20675bd91649543d2bc25b6edc1293835661f1"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 01:15:05 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 01:15:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 01:15:14 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 01:15:17 GMT
CMD ["node"]
# Thu, 15 Apr 2021 07:41:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 07:42:00 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 07:42:01 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 07:42:02 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 07:42:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 07:42:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 07:42:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 19 Apr 2021 19:13:56 GMT
ENV GHOST_VERSION=4.2.2
# Mon, 19 Apr 2021 19:21:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 19 Apr 2021 19:21:14 GMT
WORKDIR /var/lib/ghost
# Mon, 19 Apr 2021 19:21:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 19 Apr 2021 19:21:16 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 19 Apr 2021 19:21:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 19:21:18 GMT
EXPOSE 2368
# Mon, 19 Apr 2021 19:21:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c6d3ab5692397f4b3dda95b1baaabed77836f07cef0f68074ae626cb5fa4d`  
		Last Modified: Thu, 15 Apr 2021 02:04:28 GMT  
		Size: 34.8 MB (34845688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a285b9fc74e98c71f8913e67fca20895f3d28821a908e59e28b4721ac02e834c`  
		Last Modified: Thu, 15 Apr 2021 02:04:17 GMT  
		Size: 2.4 MB (2419021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6472fff65d9a1f977f0e65377ee05c476ed275dbb87420579f4350e77b7436d6`  
		Last Modified: Thu, 15 Apr 2021 02:04:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe75d9806a08fa875e7689c05018ad9f092e409344e90f291d50572bfe1270e`  
		Last Modified: Thu, 15 Apr 2021 08:03:09 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529c989854591686d4e268dbab35e5f2a9474dd36c99d8aafb102357113327e4`  
		Last Modified: Thu, 15 Apr 2021 08:03:09 GMT  
		Size: 702.7 KB (702711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0430d16567b2579bc64ec55ddfda049fcf412c31ab546a9f59ae4e749b0c85ff`  
		Last Modified: Thu, 15 Apr 2021 08:03:13 GMT  
		Size: 7.4 MB (7405660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b2c4dbab78c78a8edc8485d35eeced7ec3ebc60c9aacc8a65afb7a0c8d1086`  
		Last Modified: Mon, 19 Apr 2021 19:38:52 GMT  
		Size: 56.7 MB (56703434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc8fc0841fac2e3d4c56f260ce8991c320625623376651447ff9654049b26fe`  
		Last Modified: Mon, 19 Apr 2021 19:38:20 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:eaf658adc70df6381f16e5693d75ce2829a657af462a1d89cf0787c8ca6489fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106855689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f17cf224c1c91725ad725c5908f337cbb419997c98d997d38795f5eb1207f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:24:28 GMT
ENV NODE_VERSION=14.16.1
# Thu, 15 Apr 2021 03:34:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="39fbbd09668472f1105bdb5a7c20675bd91649543d2bc25b6edc1293835661f1"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 03:34:54 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 03:34:59 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 03:35:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:35:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:35:03 GMT
CMD ["node"]
# Thu, 15 Apr 2021 10:36:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 10:36:06 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 10:36:07 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 10:36:07 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 10:36:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 10:36:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 10:36:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 19 Apr 2021 18:59:37 GMT
ENV GHOST_VERSION=4.2.2
# Mon, 19 Apr 2021 19:06:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 19 Apr 2021 19:06:41 GMT
WORKDIR /var/lib/ghost
# Mon, 19 Apr 2021 19:06:42 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 19 Apr 2021 19:06:43 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 19 Apr 2021 19:06:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 19:06:46 GMT
EXPOSE 2368
# Mon, 19 Apr 2021 19:06:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729b33cc95bff6a339d4894936440783f6d9f9b8fcff4f656804b5f51589e099`  
		Last Modified: Thu, 15 Apr 2021 04:26:11 GMT  
		Size: 36.1 MB (36069717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feadca8c3a3527e0f48c1607c14fad7086d1e389d648d007630e05e45bf296e9`  
		Last Modified: Thu, 15 Apr 2021 04:26:02 GMT  
		Size: 2.4 MB (2426507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed996482c38503f3989d457afabe2ff764c91f3a77eecf87396d7bf2cbd823ea`  
		Last Modified: Thu, 15 Apr 2021 04:26:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f75128272534058e6663ae62a83359fd62898780ba3037f72aedf9f76837a57`  
		Last Modified: Thu, 15 Apr 2021 10:56:01 GMT  
		Size: 10.3 KB (10326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715f63a2d909696a7b5221e74df9a4f5bab12aeb033d200bdbf4d2ecd5514162`  
		Last Modified: Thu, 15 Apr 2021 10:56:03 GMT  
		Size: 824.6 KB (824615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ce871bf143aa2d55af399248e4579cda2eeb9e5870ccd3a613abec404743ee`  
		Last Modified: Thu, 15 Apr 2021 10:56:13 GMT  
		Size: 7.4 MB (7405414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7e8ec1e337ee4774cdbdda0efb41b656aacd27cbadda350c13bfb2cd4ecec`  
		Last Modified: Mon, 19 Apr 2021 19:26:37 GMT  
		Size: 57.4 MB (57406254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6443a67e5f2e7324afd6ed765bb5bcf85a090926684cf6a533ebce3a4a1ab5`  
		Last Modified: Mon, 19 Apr 2021 19:26:06 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:a2a54a31e876f2f6dbf877e100f6488b3ecd950f55d36db7d4c90406df952f58
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
$ docker pull ghost@sha256:73832c333cbc6cc70499cd418fdb84054318247585c24feaba26b636a889a89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134928781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64409a1c4e09d185e9991ffd22515ac44d08edd6c789a5c144e2e5e62a88116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:54:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 18:25:54 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 18:26:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 18:26:20 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 18:26:32 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 18:26:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 18:26:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 18:26:33 GMT
CMD ["node"]
# Thu, 12 Aug 2021 19:02:17 GMT
ENV GOSU_VERSION=1.12
# Thu, 12 Aug 2021 19:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 Aug 2021 19:02:28 GMT
ENV NODE_ENV=production
# Thu, 12 Aug 2021 19:02:28 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Thu, 12 Aug 2021 19:02:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Aug 2021 19:02:54 GMT
ENV GHOST_VERSION=4.11.0
# Thu, 12 Aug 2021 19:03:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 12 Aug 2021 19:03:49 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Aug 2021 19:03:49 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Aug 2021 19:03:49 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Thu, 12 Aug 2021 19:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 19:03:49 GMT
EXPOSE 2368
# Thu, 12 Aug 2021 19:03:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9433a176a005ffb7dc4e0d6a580852bc990b6178152675ecd4814dd6a6a72146`  
		Last Modified: Thu, 22 Jul 2021 14:06:40 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909f9fda05d6eb8bf705ba9a4bf4f5a9c917b35633cf8eb74e6acdd595b7b054`  
		Last Modified: Thu, 12 Aug 2021 18:40:51 GMT  
		Size: 35.4 MB (35384577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af9fc99b7260cc710839b8ab78ff00033edbfe29871cfdc6d47b0db2199a03`  
		Last Modified: Thu, 12 Aug 2021 18:40:46 GMT  
		Size: 2.7 MB (2733336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2744d2cf1e2363ca14a2668dab2e624922118df879b2795a664b98c0c74bd552`  
		Last Modified: Thu, 12 Aug 2021 18:40:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1585356a07d753e5a1172fda08a844c54f560f0880e2ff2fb20dcb4f5e5b908a`  
		Last Modified: Thu, 12 Aug 2021 19:09:35 GMT  
		Size: 1.4 MB (1417770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fce8d334512b8d30cd79c3e7c6ccd6dd15d143a08f72c3a3e3ce3a16975d2e`  
		Last Modified: Thu, 12 Aug 2021 19:09:38 GMT  
		Size: 9.4 MB (9403169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43a097b6efef54d34ca942479780d32a49d4b0770696aca338d06ae2c1ac22b`  
		Last Modified: Thu, 12 Aug 2021 19:09:46 GMT  
		Size: 58.8 MB (58839124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556f6441c9fb8b1c854156a6dbfafcbeec02eb628c4a9a3a169f2d693d91d903`  
		Last Modified: Thu, 12 Aug 2021 19:09:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:702bbfdb54637f4bb91a4dde3f8bf806b7e95d75f48b99fe38bf08daa6ebb2df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134316149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24f7a976a14df375f69ed159f93a9698e11d8094c823e6d5fa469741d5a2d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 23:00:30 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 23:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 23:01:34 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 23:02:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 23:02:24 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 23:02:25 GMT
CMD ["node"]
# Fri, 13 Aug 2021 08:12:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 08:13:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 08:13:29 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 08:13:29 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 08:14:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 08:14:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 08:14:15 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 08:21:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 08:21:33 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 08:21:34 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 08:21:34 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 08:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 08:21:35 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 08:21:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc4c394db31a5a2a6dd4648f088d9c406e3f6da10b16ae7a94c9cd0ab0d2a1`  
		Last Modified: Thu, 22 Jul 2021 10:12:53 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3bee9b560c58119f2fccc5a525fe07200eef8667a40c7fc4ce9a68007910d`  
		Last Modified: Fri, 13 Aug 2021 00:34:27 GMT  
		Size: 33.6 MB (33583856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d03355f4f0372dc1670aef9caca21a1de39f8c5ee8ff491ed00efda264165f9`  
		Last Modified: Fri, 13 Aug 2021 00:34:05 GMT  
		Size: 2.7 MB (2723035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6c4286b40066330b2321f01cdee653967291daf08cc3121e074ed9d6f051ff`  
		Last Modified: Fri, 13 Aug 2021 00:34:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692a9bc10bd98e1bc165cb98d33655b0ebccd1c135940f07fe0f28b75d83dc2`  
		Last Modified: Fri, 13 Aug 2021 08:53:36 GMT  
		Size: 1.4 MB (1370087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093ecaf67abbbc6fea806afe9922f38ca72874754acfdddb8db5cd648bf27e33`  
		Last Modified: Fri, 13 Aug 2021 08:53:49 GMT  
		Size: 9.4 MB (9403366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b583d3a9e7b93879a892a08ea7c52572c3d2fa44446cf349f40a411631720f5`  
		Last Modified: Fri, 13 Aug 2021 08:54:34 GMT  
		Size: 64.5 MB (64484819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aea994c24b4db86f14e1c684022befb72c030cd2975e67f675398d0785cba0d`  
		Last Modified: Fri, 13 Aug 2021 08:53:35 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0946be565f4d6c5faac6bc4c9787d87acd422298c7cf46cafe60b507e9c3c859
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133232069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07775c88fc91a454477ce2947a9a7242d77e1f0140f6ffc79e601c2cfff35fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:52:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 13 Aug 2021 00:34:34 GMT
ENV NODE_VERSION=14.17.5
# Fri, 13 Aug 2021 00:34:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Fri, 13 Aug 2021 00:35:00 GMT
ENV YARN_VERSION=1.22.5
# Fri, 13 Aug 2021 00:35:17 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Fri, 13 Aug 2021 00:35:17 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 13 Aug 2021 00:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 00:35:17 GMT
CMD ["node"]
# Fri, 13 Aug 2021 05:15:38 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 05:16:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 05:16:02 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 05:16:02 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 05:16:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 05:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 05:16:26 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 05:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 05:19:35 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 05:19:36 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 05:19:36 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5feabdf4457afcbb173afd2eca18467be8d8fd18b5199dd8b508c76994f3bc`  
		Last Modified: Thu, 22 Jul 2021 05:07:38 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f852c7ad0a132bc2311af4000aae71873bdaa05cb79e33ce6e90fbcb58c7c792`  
		Last Modified: Fri, 13 Aug 2021 02:52:14 GMT  
		Size: 35.5 MB (35500636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb2ca6c9cf2688290d19a82507ad79b3c48f0ced478879b25ef003b9701de4`  
		Last Modified: Fri, 13 Aug 2021 02:52:08 GMT  
		Size: 2.7 MB (2733181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6373680b3d9077dfd1a3e6e7d89797f48f77a3a0306dcc72be7622da027355fc`  
		Last Modified: Fri, 13 Aug 2021 02:52:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ca739efd0ac0d79e8ddf7a0ce7379b7d90d881439501658c836620eefe82c`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 1.4 MB (1353087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2d192a41d98b86f0d6ccde6896569f891eb39a7fd9a480882a439ccaf04c48`  
		Last Modified: Fri, 13 Aug 2021 05:35:49 GMT  
		Size: 9.4 MB (9403397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88ca1e8a30bed4ea6d000e0fe4766c9dba5497910593aa5f7989cd2c9fe115d`  
		Last Modified: Fri, 13 Aug 2021 05:36:00 GMT  
		Size: 58.3 MB (58321953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed45096bb3714dbea9fa1f475bc9be52f6357c87c94110aa336e865636c40b0d`  
		Last Modified: Fri, 13 Aug 2021 05:35:47 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:641d5468b043638f2e85eee8f692f15b6052d4be38a5bf101839417906d8cc6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7568b69fe7bb516732ad18fbaac029f4d0e7c7beadfb19465e2f1a36a2d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:55:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:07:56 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:13:31 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:17:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:17:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:17:50 GMT
CMD ["node"]
# Fri, 13 Aug 2021 03:42:29 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 03:44:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 03:44:58 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 03:45:08 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 03:46:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 03:47:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 03:47:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 03:47:11 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 04:14:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 04:14:57 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 04:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 04:15:02 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 04:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 04:15:10 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 04:15:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad84eba8f7b883015349631ae1d1de803b37e838243439abb789d2bc8ff587`  
		Last Modified: Thu, 22 Jul 2021 12:12:52 GMT  
		Size: 4.2 KB (4192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700700ba2d5aa928042009517157d005113c5294d9955507dda41cee2208ec0`  
		Last Modified: Fri, 13 Aug 2021 00:01:16 GMT  
		Size: 37.3 MB (37290566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150545c38e67102af6dbfae496efb15bbcc63e022d2c0874ad097a50bf8174c2`  
		Last Modified: Fri, 13 Aug 2021 00:00:19 GMT  
		Size: 2.7 MB (2734176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cac311421ba89abfb0ad0936386b31a47f151ad1db601b54f5b8769e8c96f4`  
		Last Modified: Fri, 13 Aug 2021 00:00:18 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcc999bcbd77fb0870285ab4e8bd86626d86f0d8a9d452d50a89f4fcc7f5dc6`  
		Last Modified: Fri, 13 Aug 2021 04:46:22 GMT  
		Size: 1.3 MB (1338766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7feaaaf058e300baaa0b9c338c1a6c6b13945d8014805af9d4f38dc5a7cc69`  
		Last Modified: Fri, 13 Aug 2021 04:47:43 GMT  
		Size: 9.4 MB (9403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3110289d82b47fbc91a92a5b43dea938fad2c5f72f21ea1442420692e99d414`  
		Last Modified: Fri, 13 Aug 2021 04:48:46 GMT  
		Size: 59.8 MB (59763172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296655aad5db71b12e50630876096352650e0da37f79912bbaa68cb49c432f28`  
		Last Modified: Fri, 13 Aug 2021 04:46:20 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:84cab829540ac78b1482e011037a87a49aa4a9bdfb020339c86c465234c9fa9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133832121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c30070a4db8effe061a38e325de3ca0eeec2fce6413948c11e8f9730b1eecc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:05:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 12 Aug 2021 22:58:33 GMT
ENV NODE_VERSION=14.17.5
# Thu, 12 Aug 2021 22:59:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Thu, 12 Aug 2021 22:59:03 GMT
ENV YARN_VERSION=1.22.5
# Thu, 12 Aug 2021 22:59:19 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Thu, 12 Aug 2021 22:59:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:59:20 GMT
CMD ["node"]
# Fri, 13 Aug 2021 02:58:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 13 Aug 2021 02:58:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Aug 2021 02:58:43 GMT
ENV NODE_ENV=production
# Fri, 13 Aug 2021 02:58:43 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Fri, 13 Aug 2021 02:59:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 13 Aug 2021 02:59:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Aug 2021 02:59:16 GMT
ENV GHOST_VERSION=4.11.0
# Fri, 13 Aug 2021 03:05:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! gosu node yarn add "sqlite3@$sqlite3Version" --force; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends g++ gcc libc-dev libvips-dev make python3; 		rm -rf /var/lib/apt/lists/*; 				npm_config_python='python3' gosu node yarn add "sqlite3@$sqlite3Version" --force --build-from-source --ignore-optional; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 13 Aug 2021 03:05:31 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Aug 2021 03:05:32 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Aug 2021 03:05:32 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Fri, 13 Aug 2021 03:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 03:05:33 GMT
EXPOSE 2368
# Fri, 13 Aug 2021 03:05:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2262a8cff9db9c0ebe52a2bc091c48afd45289f3370dbf352d8b6ba846770a35`  
		Last Modified: Thu, 22 Jul 2021 03:21:06 GMT  
		Size: 4.2 KB (4196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52586f67f92f8b93c0e5a326fbba79b340d9770d07e28e36bf13901ae445205`  
		Last Modified: Fri, 13 Aug 2021 00:22:08 GMT  
		Size: 35.3 MB (35261198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31332acb30d45a9c3946e3f1b33141bb5a7210cbf9e47468ffc322bc187f53`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 2.7 MB (2734870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2477a2e9f332d95dc46a743f115fcda854c78487acdbce98af315b2844f170b`  
		Last Modified: Fri, 13 Aug 2021 00:22:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e35573df8a50fce6e878e4d1ea1d3f6163644023eb3092484069802b96eacb`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 1.4 MB (1404613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a165afdcafe23870ba965f4ceff95f436b153a706db5f448b895693dbdf555b0`  
		Last Modified: Fri, 13 Aug 2021 03:12:12 GMT  
		Size: 9.4 MB (9403269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c4d1b5e54d963852f6f5a21a14ce9d46301f11d38d8064e071f29fc97dce3`  
		Last Modified: Fri, 13 Aug 2021 03:12:21 GMT  
		Size: 59.3 MB (59262383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332145ac6b77a8d7c747fbada3da2a07fa8b4b832b8f4fe5881887bbe4e46f97`  
		Last Modified: Fri, 13 Aug 2021 03:12:10 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

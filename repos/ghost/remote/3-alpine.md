## `ghost:3-alpine`

```console
$ docker pull ghost@sha256:17abfa5291daed623173d6673d14a45415487297e37e24ece9a507d6d0715e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:3-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:59f4c441d4e347c6470bb520c6179fef5b07fc1467928f50b4672eae8efd3529
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112229299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a9f73fb11dc33fb7f43506e26ed851987ccc3a630633be4d5760fcda3cb81b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 19:58:37 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 19:58:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 19:58:45 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 19:58:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 19:58:50 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 19:58:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 19:58:50 GMT
CMD ["node"]
# Tue, 24 Dec 2019 21:04:36 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 21:04:39 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 21:04:40 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 21:04:40 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 21:05:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 21:05:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 21:05:09 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 21:05:10 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 21:06:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 21:06:55 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 21:06:56 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 21:06:56 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 21:06:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 21:06:57 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 21:06:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616b6dd285e6b348060fbe763820dc2efe320f31349dd3681be366d4819d5050`  
		Last Modified: Tue, 24 Dec 2019 20:01:16 GMT  
		Size: 22.5 MB (22525582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c84100e8e0b17c3db2f3e7aebce5beb6deabf66f4c143f6af459d610af2532`  
		Last Modified: Tue, 24 Dec 2019 20:01:11 GMT  
		Size: 1.3 MB (1264627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5cb4d1ea5ac733fff55eae6b81447fc0fffb8e1d678af93dddfe79ba083d56`  
		Last Modified: Tue, 24 Dec 2019 20:01:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e9c9cc9246e85c3aeb9f172f98e6cb95f1a2d3fe6fa4caf4d3aa0921f4adc8`  
		Last Modified: Tue, 24 Dec 2019 21:11:55 GMT  
		Size: 9.9 KB (9907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4c86033b26c7f1d1485cc8adb64e07624d17fd41635be195ee464df398ef5`  
		Last Modified: Tue, 24 Dec 2019 21:11:56 GMT  
		Size: 1.2 MB (1211046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ff97e25cddc81de0c521520893d70b8ee9c4ef593580cb8c04f7827105762a`  
		Last Modified: Tue, 24 Dec 2019 21:12:01 GMT  
		Size: 6.8 MB (6788424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653088ab8d5a10ecf4bc91f86c4ee5b637df7de8996ad2deafb24e6550c2a6ab`  
		Last Modified: Tue, 24 Dec 2019 21:12:19 GMT  
		Size: 77.6 MB (77627111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa5543852625ba448775ccbcd836908771f515aad102f0749c1e6f9188f2c2a`  
		Last Modified: Tue, 24 Dec 2019 21:11:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:11555bfcb125550652dc56254d1e1826466c4edf5a7b60be3a1e5e6934356bc9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103135523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed432459554410e7efc14d1a507c39337e29b2763bc93b046699184cd36c687`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:42:01 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 20:48:21 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 20:48:23 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 20:48:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 20:48:28 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:48:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:48:29 GMT
CMD ["node"]
# Tue, 24 Dec 2019 21:05:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 21:05:48 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 21:05:49 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 21:05:50 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 21:06:34 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 21:06:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 21:06:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 21:06:38 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 21:12:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 21:12:40 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 21:12:41 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 21:12:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 21:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 21:12:42 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 21:12:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a54325157e65f3d815e610314a70414fae410630b6929ad3acafec45845e897`  
		Last Modified: Tue, 24 Dec 2019 20:50:00 GMT  
		Size: 22.0 MB (21986182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84192ba1702ce6296521da7d14050a38e8dc0eed40a4107c39f6413d8bf7ed20`  
		Last Modified: Tue, 24 Dec 2019 20:49:55 GMT  
		Size: 1.3 MB (1327803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373b28b52438181ad3ce48938f85f6c4d108b6d1110dac97ddace5fec95a3de8`  
		Last Modified: Tue, 24 Dec 2019 20:49:55 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba9f982a2f158c365696f1fc82e3eaa763f223b9a6ee57b822d8772c6d1a3d`  
		Last Modified: Tue, 24 Dec 2019 21:32:08 GMT  
		Size: 9.7 KB (9730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c821f6e3fe8e5ceca375cb1013af3ebc5206a5582ad6abd1a0f3183ee55298`  
		Last Modified: Tue, 24 Dec 2019 21:32:09 GMT  
		Size: 1.2 MB (1162960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a867e925158cea663a5ae39625b9668f862992c17e52f897d5b5e3c0f6ff9153`  
		Last Modified: Tue, 24 Dec 2019 21:32:12 GMT  
		Size: 6.8 MB (6788386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79e37642cf404a719cb85473ea18d3d23fc1b04d25e2dd8813ace525e8502b`  
		Last Modified: Tue, 24 Dec 2019 21:32:35 GMT  
		Size: 69.2 MB (69247615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e4bca83b75f9826b7b84a48f1e3adbaa95875073da892e21bd619c18929812`  
		Last Modified: Tue, 24 Dec 2019 21:32:08 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:50702f720c68a866672fb7d0a2198fb795e6d6212054e525c6bdb9e8ce653101
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101570683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9c9e28118ca340524b7efcf0dc0027c565a9c960596bd1167017a77dad884b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:05:22 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 20:10:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 20:10:24 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 20:10:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 20:10:29 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:10:30 GMT
CMD ["node"]
# Tue, 24 Dec 2019 21:58:31 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 21:58:35 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 21:58:37 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 21:58:39 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 21:59:10 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 21:59:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 21:59:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 21:59:15 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 22:03:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 22:03:42 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 22:03:43 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 22:03:43 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 22:03:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:03:45 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 22:03:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc3521389e6fdd97a9afd70243e571cdf1fa4ad49d2151de7760124d141a951`  
		Last Modified: Tue, 24 Dec 2019 20:13:27 GMT  
		Size: 21.6 MB (21588310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e223b97e3f60b64925d93314f26058ebd546deca2f903c3e712ce72400d49a`  
		Last Modified: Tue, 24 Dec 2019 20:13:20 GMT  
		Size: 1.3 MB (1327760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47b9468e3525f8076eb7b16973581180094e01e53dc8c693c49681ea8801935`  
		Last Modified: Tue, 24 Dec 2019 20:13:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824f6d4a45ffff767ed26c8cd2dc45091148a9b5dcbfbec085fee4a6b5cf795`  
		Last Modified: Tue, 24 Dec 2019 22:16:06 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa468e14e8c2b7ae1eddda2c07de64e561ba370c14fe300e880402bb6c4e5d5`  
		Last Modified: Tue, 24 Dec 2019 22:16:07 GMT  
		Size: 1.1 MB (1101462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707bd63aef29da5295bae4ded0ccdc2f353da61d977e855b8f242d1d725dce3e`  
		Last Modified: Tue, 24 Dec 2019 22:16:11 GMT  
		Size: 6.8 MB (6787934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db811b8f606a56ad72f5b28b5f5d73397b446c1d97c40e9af42b55180007134f`  
		Last Modified: Tue, 24 Dec 2019 22:16:29 GMT  
		Size: 68.3 MB (68338179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9abffbbc1789b07937786a00a5d1377b2bb09c28fbbe9a283f26a5af83b807`  
		Last Modified: Tue, 24 Dec 2019 22:16:06 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f069d87efd419bc6498eb35a65a379c79e7cd076cae0904353dd37703a82b81c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104413743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97ad68bcb4215a9b75067a7dea801f2c8d9bcc6b4d8b7f0fb3fa33a87e0c715`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 22:10:41 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 22:16:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 22:16:46 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 22:16:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 22:16:51 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:16:52 GMT
CMD ["node"]
# Tue, 24 Dec 2019 22:37:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 22:37:17 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 22:37:19 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 22:37:19 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 22:37:43 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 22:37:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 22:37:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 22:37:47 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 22:42:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 22:42:07 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 22:42:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 22:42:08 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 22:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:42:09 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 22:42:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aea54cb4a6ad43b3c32366335371115297a6a0b7deaebb79d0a246cd656a7d`  
		Last Modified: Tue, 24 Dec 2019 22:19:59 GMT  
		Size: 22.8 MB (22812301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955731e15cb47b2690ffaea9bc9817b0f2c2630ec21bc8c852bb50c2f0e96fe4`  
		Last Modified: Tue, 24 Dec 2019 22:19:52 GMT  
		Size: 1.3 MB (1327701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17856ae50ffad491ee482c47a32f50a5279704ebd79e9b863cf0c879ccb0af63`  
		Last Modified: Tue, 24 Dec 2019 22:19:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a845504bfe740843adc2d697eb8786c45d0f5ef625c3378a21d49b43e64f6705`  
		Last Modified: Tue, 24 Dec 2019 22:52:28 GMT  
		Size: 9.8 KB (9846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa1875e195faf89fba75ef096f3b46b69edfb01530e514b93858f51a30c7074`  
		Last Modified: Tue, 24 Dec 2019 22:52:28 GMT  
		Size: 1.2 MB (1223198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2195f46c2f2ab2cb33f510186a6087d6d173df97218846e3182c274fe64fba01`  
		Last Modified: Tue, 24 Dec 2019 22:52:31 GMT  
		Size: 6.8 MB (6787607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfafe0b7ec34c9b0ef1c997337eb2bbaeef467ded3a821902fbca40073363210`  
		Last Modified: Tue, 24 Dec 2019 22:52:49 GMT  
		Size: 69.5 MB (69533083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a96a57c5c610424b9721d4ae2c7127c51dc0ee49a176cee97680fdac1b0aa`  
		Last Modified: Tue, 24 Dec 2019 22:52:28 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; 386

```console
$ docker pull ghost@sha256:907d4396ec9b500d4b8ce76a42004b2034b4d5142c88843d59bc5a5fe3faccba
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f97ac187d659637012e15369ca04b1117220db69d663411be8058868888afed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 22:00:55 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 22:29:52 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 22:29:52 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 22:29:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 22:29:55 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 22:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:29:56 GMT
CMD ["node"]
# Tue, 24 Dec 2019 22:59:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 22:59:43 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 22:59:44 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 22:59:44 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 22:59:59 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 22:59:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 23:00:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 23:00:00 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 23:03:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 23:03:31 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 23:03:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 23:03:32 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 23:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 23:03:32 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 23:03:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa91495fe503367e40ce3876fbb7a17462423569993a994e3db1ea24f9de821c`  
		Last Modified: Tue, 24 Dec 2019 22:31:28 GMT  
		Size: 22.8 MB (22772227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2988b10eab07d05b99658c231f678ae1f9a0fbf0c7fc464e49d8460860bf98`  
		Last Modified: Tue, 24 Dec 2019 22:31:23 GMT  
		Size: 1.3 MB (1327788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921a6d7d71ef53c7f264b9c8416c7b6b13bb25713e9a688b56b4b680095163a`  
		Last Modified: Tue, 24 Dec 2019 22:31:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c069aad64b0c404994c88227ae166fdd8d37c51fc33cd7667e57a783654f95`  
		Last Modified: Tue, 24 Dec 2019 23:07:49 GMT  
		Size: 10.0 KB (9980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd5c8371c2bdcedd249039c6e357ff0945c796c3f1c5432fe2e37772808c308`  
		Last Modified: Tue, 24 Dec 2019 23:07:50 GMT  
		Size: 1.3 MB (1261253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9552760f30223e454d294be470fd5b98b6cecb59a3f75d8a5f1f376cc894612`  
		Last Modified: Tue, 24 Dec 2019 23:07:54 GMT  
		Size: 6.8 MB (6787695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359a283fb59b6be569004bd7829c8815b1403071d79765530cc2a907f4aa83f2`  
		Last Modified: Tue, 24 Dec 2019 23:08:13 GMT  
		Size: 69.7 MB (69671465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8244aa4520711d4ca6fe221b5cc0cd835e945b77dc5d4c650c942a98afdbda`  
		Last Modified: Tue, 24 Dec 2019 23:07:50 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; ppc64le

```console
$ docker pull ghost@sha256:0d066104f19bff24bd8fb3803c47977ec49556168196a04bdcc3000963f35a45
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108033254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cd5f55e9f30217262c29d63805fd14331134219ed35e85e5773fc633614e42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 22:09:50 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 22:22:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 22:22:06 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 22:22:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 22:22:14 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 22:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:22:17 GMT
CMD ["node"]
# Tue, 24 Dec 2019 22:44:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 22:44:57 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 22:44:59 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 22:45:01 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 22:45:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 22:45:31 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 22:45:33 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 22:45:35 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 22:49:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 22:49:35 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 22:49:38 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 22:49:39 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 22:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:49:45 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 22:49:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f21eece5915e09f2b6924f4dc5e4e75be16194e079fc2652ada1a46df69e96`  
		Last Modified: Tue, 24 Dec 2019 22:27:12 GMT  
		Size: 24.5 MB (24532561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807441770c6e87d6893839024973f7097679eb90eb7c6be3baeffbf0a0bb3e85`  
		Last Modified: Tue, 24 Dec 2019 22:27:07 GMT  
		Size: 1.3 MB (1327757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e9b0a80934af5a1064e15b0c91c8afc27ea38d9c9545a10566b339796f34c`  
		Last Modified: Tue, 24 Dec 2019 22:27:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bd75927719fdaf671d9e517bd6be4398b24db85b481b06b17e0007531d8cca`  
		Last Modified: Tue, 24 Dec 2019 23:07:03 GMT  
		Size: 10.4 KB (10395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d04fbaa026d967af1a47255897bbcd8e1005bd659fefebaa9e1ed029056824`  
		Last Modified: Tue, 24 Dec 2019 23:07:05 GMT  
		Size: 1.3 MB (1293094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d441917f7106adeb370452352e3dfba6924a34960d938385ca9f4ae15bfc9ff`  
		Last Modified: Tue, 24 Dec 2019 23:07:20 GMT  
		Size: 6.8 MB (6787761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc80dec7a0ae56db11f936b4bca12045c5ad553bceabc760315b7d2ed30962c`  
		Last Modified: Tue, 24 Dec 2019 23:07:48 GMT  
		Size: 71.3 MB (71264376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629a0cc3df1da7cfab2c498a977d732559e536c8e460c960c122c59ce9bd347`  
		Last Modified: Tue, 24 Dec 2019 23:07:03 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; s390x

```console
$ docker pull ghost@sha256:d8cf1ebcb16d89ce10ea9d9fdabdd101df0ad40c24b2eebf2be1bab4faed99dd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103928527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3b5ed894f0abdbf34ec5d220921060ec9747850c8d49e3b0feb5a83522422b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 20:16:56 GMT
ADD file:d26fbcd308b78da175af74382b16ee1f7a3370ab9d618b306d604d292e72c560 in / 
# Tue, 24 Dec 2019 20:16:56 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 21:34:46 GMT
ENV NODE_VERSION=10.18.0
# Tue, 24 Dec 2019 21:45:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Tue, 24 Dec 2019 21:45:31 GMT
ENV YARN_VERSION=1.21.1
# Tue, 24 Dec 2019 21:45:33 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 24 Dec 2019 21:45:33 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 24 Dec 2019 21:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 21:45:33 GMT
CMD ["node"]
# Tue, 24 Dec 2019 22:03:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 24 Dec 2019 22:03:49 GMT
RUN apk add --no-cache 		bash
# Tue, 24 Dec 2019 22:03:49 GMT
ENV NODE_ENV=production
# Tue, 24 Dec 2019 22:03:49 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Tue, 24 Dec 2019 22:04:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 24 Dec 2019 22:04:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Dec 2019 22:04:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Dec 2019 22:04:01 GMT
ENV GHOST_VERSION=3.2.0
# Tue, 24 Dec 2019 22:09:11 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 24 Dec 2019 22:09:12 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Dec 2019 22:09:12 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Dec 2019 22:09:13 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 24 Dec 2019 22:09:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:09:13 GMT
EXPOSE 2368
# Tue, 24 Dec 2019 22:09:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bca389ebb9be8103bf737251d68f962104771b2f9c1fff1f7ae0207458fa4c86`  
		Last Modified: Tue, 24 Dec 2019 20:17:18 GMT  
		Size: 2.6 MB (2579591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6065501d709f01e226e711d3ebd5a62f81b154d77c4c3d22a2231efd972cd19d`  
		Last Modified: Tue, 24 Dec 2019 21:47:16 GMT  
		Size: 22.6 MB (22597373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5cfc83c630dec98c0e686f25e8aa3004ed75fdf96a539de88e73c462606c29`  
		Last Modified: Tue, 24 Dec 2019 21:47:12 GMT  
		Size: 1.3 MB (1327725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66532cb179e7d0e5f64a238cd305fb9db9f6d1e337e998af14a51cb5c5ad96cf`  
		Last Modified: Tue, 24 Dec 2019 21:47:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a37f2879ac332dc143b02698e46180759b90391693db31260efa150093d2f`  
		Last Modified: Tue, 24 Dec 2019 22:13:28 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e646bb1306b4b6deac82a9d2c38937a3e9612358256eae5f19e590da71a02e3a`  
		Last Modified: Tue, 24 Dec 2019 22:13:28 GMT  
		Size: 1.2 MB (1245171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825b5049b26fa3f18b2d9fc3f9db4ec50f5bee9aa602aade3aa9d5cded5bc78f`  
		Last Modified: Tue, 24 Dec 2019 22:13:29 GMT  
		Size: 6.8 MB (6786778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d659f55193c35f5cc06a325c41d6a894e12a467ad63aeabcef4bc5939941bcf8`  
		Last Modified: Tue, 24 Dec 2019 22:13:37 GMT  
		Size: 69.4 MB (69381080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8fb68b3a95883c00719da00ba1e982dd2f2906c6f5f26a7f579ef0ece3a51a`  
		Last Modified: Tue, 24 Dec 2019 22:13:28 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

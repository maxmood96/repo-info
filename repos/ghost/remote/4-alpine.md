## `ghost:4-alpine`

```console
$ docker pull ghost@sha256:fde5fb65cef108a14d3a1b99ffcc7d53b9609351f66e9d4fcfc592201b371e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:12719d76575cbc9d3c07f4a3ee094e079ad404d1455d115bcd40524b26e65219
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117651366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fe78e36a49bb159f6558564281e3ded4a40e56ef60a3ebcae0754845e8c426`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 21:16:02 GMT
ENV NODE_VERSION=14.18.3
# Tue, 11 Jan 2022 21:16:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5e148aaf5f728f38ded2daa20b0844e3afd422cf9dd6072958e476cf7437c5f3"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 21:16:12 GMT
ENV YARN_VERSION=1.22.15
# Tue, 11 Jan 2022 22:25:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 22:25:13 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 22:25:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 22:25:13 GMT
CMD ["node"]
# Tue, 11 Jan 2022 22:33:39 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 11 Jan 2022 22:33:40 GMT
RUN apk add --no-cache 		bash
# Tue, 11 Jan 2022 22:33:40 GMT
ENV NODE_ENV=production
# Tue, 11 Jan 2022 22:33:40 GMT
ENV GHOST_CLI_VERSION=1.18.1
# Tue, 11 Jan 2022 22:34:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 11 Jan 2022 22:34:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 11 Jan 2022 22:34:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 28 Jan 2022 23:22:24 GMT
ENV GHOST_VERSION=4.34.0
# Fri, 28 Jan 2022 23:23:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 28 Jan 2022 23:23:38 GMT
WORKDIR /var/lib/ghost
# Fri, 28 Jan 2022 23:23:38 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 28 Jan 2022 23:23:38 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 28 Jan 2022 23:23:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jan 2022 23:23:39 GMT
EXPOSE 2368
# Fri, 28 Jan 2022 23:23:39 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d19c7b532d498095829b665d2c541f9a04cc3bed80978a2412eb0c45ca20e61`  
		Last Modified: Tue, 11 Jan 2022 22:29:52 GMT  
		Size: 36.7 MB (36682145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12099b9f251c343defeee0c7d9c907f3cb9084153477efc827a5a1f763f17da`  
		Last Modified: Tue, 11 Jan 2022 22:29:45 GMT  
		Size: 2.4 MB (2368147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fb97b6952fad21ee9052f1641b6d90e3520a1dc7e5bda42d5d7558c8943437`  
		Last Modified: Tue, 11 Jan 2022 22:29:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed54144d2b0bb55d0133999c9b79366375760684afd42df5f300fd83cf705eb`  
		Last Modified: Tue, 11 Jan 2022 22:39:21 GMT  
		Size: 11.2 KB (11215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c7a96f67bf1b3726377b4f72b706340ee7d5c2c1d5acdf8f08b86480c98552`  
		Last Modified: Tue, 11 Jan 2022 22:39:22 GMT  
		Size: 816.9 KB (816873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8289ffa94387f46226cc228fe16eeb648cdd18056f781a9296e3abf8105e66a`  
		Last Modified: Tue, 11 Jan 2022 22:39:25 GMT  
		Size: 9.4 MB (9426473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd92d7c8f94c2fc44f6611fe395ee3bed38242339ad2140522a97d053111f90`  
		Last Modified: Fri, 28 Jan 2022 23:24:48 GMT  
		Size: 65.5 MB (65522530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4184d6c3ecbdd7076b1fbc665f6080f4956511660b652b46013fd3199b51ac6`  
		Last Modified: Fri, 28 Jan 2022 23:24:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:d044fd94d3ce9358108eca858355d4b0992946e50ddf791f3dffb6605bc59459
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119130171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6263d7efd5018689b508bd8c1d3fbee13511c4c2c3baa101d0c320a884873969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 20:50:45 GMT
ENV NODE_VERSION=14.18.3
# Tue, 11 Jan 2022 21:08:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5e148aaf5f728f38ded2daa20b0844e3afd422cf9dd6072958e476cf7437c5f3"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 21:08:24 GMT
ENV YARN_VERSION=1.22.15
# Tue, 11 Jan 2022 21:08:38 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 21:08:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 21:08:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 21:08:40 GMT
CMD ["node"]
# Tue, 11 Jan 2022 22:34:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 11 Jan 2022 22:34:49 GMT
RUN apk add --no-cache 		bash
# Tue, 11 Jan 2022 22:34:50 GMT
ENV NODE_ENV=production
# Tue, 11 Jan 2022 22:34:50 GMT
ENV GHOST_CLI_VERSION=1.18.1
# Tue, 11 Jan 2022 22:36:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 11 Jan 2022 22:36:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 11 Jan 2022 22:36:06 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 28 Jan 2022 22:49:35 GMT
ENV GHOST_VERSION=4.34.0
# Fri, 28 Jan 2022 22:58:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 28 Jan 2022 22:58:35 GMT
WORKDIR /var/lib/ghost
# Fri, 28 Jan 2022 22:58:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 28 Jan 2022 22:58:36 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 28 Jan 2022 22:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jan 2022 22:58:37 GMT
EXPOSE 2368
# Fri, 28 Jan 2022 22:58:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b2771cd1780c1ac544ef3bbfd97713fe7a53a3b0b1602c865784d28042397`  
		Last Modified: Tue, 11 Jan 2022 22:06:52 GMT  
		Size: 35.7 MB (35743456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce8ee973f1b5479f787bf263074f881c27253a9841fbda0f27268725690153`  
		Last Modified: Tue, 11 Jan 2022 22:06:29 GMT  
		Size: 2.4 MB (2418916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44fffeb6f4d6c718e425fdae95865d97ee1b859d8be203202f259a4fb0e0201`  
		Last Modified: Tue, 11 Jan 2022 22:06:27 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85b5bb119651ab03d8f4880ebb939b3bb199bf5292e79e51beb012727dd260c`  
		Last Modified: Fri, 14 Jan 2022 01:10:20 GMT  
		Size: 11.0 KB (10986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c31600ed1fa05aa502d16792277d6429eb851fbb4662c5bb3308ee9f16bb3b`  
		Last Modified: Fri, 14 Jan 2022 01:10:21 GMT  
		Size: 771.0 KB (770950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee66dec73b0e43ab6600a82ab26be4457190f9ab8ac2c78cec57ef892e52743`  
		Last Modified: Fri, 14 Jan 2022 01:10:35 GMT  
		Size: 9.4 MB (9426232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0936639b04d512924a23aabb923e233f0f21d3bf5d287b8895ff2d20848a34b`  
		Last Modified: Fri, 28 Jan 2022 23:00:47 GMT  
		Size: 68.1 MB (68123245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaf2532ecc8f3c5bcf7bb0d5b40463b05ab68300d619fbe24665859fd26313b`  
		Last Modified: Fri, 28 Jan 2022 22:59:32 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:ce91745d09ba50539c775d206a6fb7e2b37a8bbabb1ea28022492f4c952ce067
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117889719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f406a10ddfb21e9a6c96cfe85fae6c241e02e5f4d8272f32b4a9bdc297c5a9e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 19:54:06 GMT
ENV NODE_VERSION=14.18.3
# Tue, 11 Jan 2022 20:14:52 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5e148aaf5f728f38ded2daa20b0844e3afd422cf9dd6072958e476cf7437c5f3"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 20:14:53 GMT
ENV YARN_VERSION=1.22.15
# Tue, 11 Jan 2022 20:15:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 20:15:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 20:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 20:15:06 GMT
CMD ["node"]
# Wed, 12 Jan 2022 01:03:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 12 Jan 2022 01:03:50 GMT
RUN apk add --no-cache 		bash
# Wed, 12 Jan 2022 01:03:50 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 01:03:51 GMT
ENV GHOST_CLI_VERSION=1.18.1
# Wed, 12 Jan 2022 01:04:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 12 Jan 2022 01:04:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 12 Jan 2022 01:04:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 28 Jan 2022 23:06:17 GMT
ENV GHOST_VERSION=4.34.0
# Fri, 28 Jan 2022 23:13:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 28 Jan 2022 23:13:36 GMT
WORKDIR /var/lib/ghost
# Fri, 28 Jan 2022 23:13:37 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 28 Jan 2022 23:13:37 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 28 Jan 2022 23:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jan 2022 23:13:38 GMT
EXPOSE 2368
# Fri, 28 Jan 2022 23:13:39 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381f181c341538c05eeb2945e04bf42eb0ab96c0a2b7c1ab5b2e2aee370a51b6`  
		Last Modified: Tue, 11 Jan 2022 21:59:17 GMT  
		Size: 35.3 MB (35288006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d20f598817d6c358d0c863f761fd676c7a1f4303a571a087d3902d2ceb67a95`  
		Last Modified: Tue, 11 Jan 2022 21:58:54 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba160ac497efef4a869768e0d613db3959fdd7fc79d0ffea31d1b8e7dce6563`  
		Last Modified: Tue, 11 Jan 2022 21:58:53 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290267af8bb0563234180577c2a6f83f28fe921e5c6a8f0caef67b3b1115693`  
		Last Modified: Fri, 14 Jan 2022 01:52:01 GMT  
		Size: 10.8 KB (10788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe274ec3a5b4ece0efb252b2d94577bfb4b5c45c2b4102d4ebe9ea98711f682`  
		Last Modified: Fri, 14 Jan 2022 01:52:01 GMT  
		Size: 703.9 KB (703914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf7874fc7ca73aa109b7bd2a795d6ac03bfc3b733cf491508250d897c4177e5`  
		Last Modified: Fri, 14 Jan 2022 01:52:16 GMT  
		Size: 9.4 MB (9426435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4c1c6abee2afc1047825bf2106f071a9a0b9fec292ff40158e6b2e53eb1c27`  
		Last Modified: Fri, 28 Jan 2022 23:18:01 GMT  
		Size: 67.6 MB (67601900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4cb174f8335d40771701ce3c0a89aba029697e8c233915f9c2962a6063f34`  
		Last Modified: Fri, 28 Jan 2022 23:16:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:316ce1de95ce020364829cec398085373604b2edf1d06498abadb5789d79fd99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136827341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474f49159683f5da3175ee180b8dc653b8a33d7d433998ef59cf6035809fda36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 21:45:54 GMT
ENV NODE_VERSION=14.18.3
# Tue, 11 Jan 2022 22:05:47 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5e148aaf5f728f38ded2daa20b0844e3afd422cf9dd6072958e476cf7437c5f3"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 22:05:47 GMT
ENV YARN_VERSION=1.22.15
# Tue, 11 Jan 2022 22:05:53 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 22:05:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 22:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 22:05:56 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:41:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 12 Jan 2022 00:41:59 GMT
RUN apk add --no-cache 		bash
# Wed, 12 Jan 2022 00:41:59 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:42:00 GMT
ENV GHOST_CLI_VERSION=1.18.1
# Wed, 12 Jan 2022 00:42:24 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 12 Jan 2022 00:42:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 12 Jan 2022 00:42:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 28 Jan 2022 23:45:05 GMT
ENV GHOST_VERSION=4.34.0
# Fri, 28 Jan 2022 23:48:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 28 Jan 2022 23:48:33 GMT
WORKDIR /var/lib/ghost
# Fri, 28 Jan 2022 23:48:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 28 Jan 2022 23:48:38 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 28 Jan 2022 23:48:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jan 2022 23:48:43 GMT
EXPOSE 2368
# Fri, 28 Jan 2022 23:48:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b6a8f5d5a5e9ec0b2fea523fcf8250ccef9296059c026b7b4829af9ebccfec`  
		Last Modified: Tue, 11 Jan 2022 23:25:35 GMT  
		Size: 36.6 MB (36553047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de100b2e390b8868b9fd5c82b81d662b31e691360d866c945808c9c7b312214d`  
		Last Modified: Tue, 11 Jan 2022 23:25:30 GMT  
		Size: 2.4 MB (2426693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb6f64cd226017440f706415a4d83e74d60881e1288d3c8591b244984eee09c`  
		Last Modified: Tue, 11 Jan 2022 23:25:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9460eb642c4c2a2a1e8e6ef294ec9419da0b5da87651da35b736a27cc8a690`  
		Last Modified: Fri, 14 Jan 2022 01:04:37 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d361914abb0ef1ff54c25454c617722e2fb7e7ace43673b900c4470b549ebe`  
		Last Modified: Fri, 14 Jan 2022 01:04:38 GMT  
		Size: 826.1 KB (826063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ab6bafc53a71839e3515db35fb411f34eaece31b4418dd3a67c6fac3dbddd0`  
		Last Modified: Fri, 14 Jan 2022 01:04:40 GMT  
		Size: 9.4 MB (9426305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e22a3f59ed2a4abffaf7748941f66eab0493f2bac85b62954ac760b4c0ba7f`  
		Last Modified: Fri, 28 Jan 2022 23:50:28 GMT  
		Size: 84.9 MB (84865528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947cace37cf44d223ef55fbf0db1b5fd81472bb641adf3eb9b2ab7547019930b`  
		Last Modified: Fri, 28 Jan 2022 23:50:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

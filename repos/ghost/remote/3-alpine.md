## `ghost:3-alpine`

```console
$ docker pull ghost@sha256:3b099b04bc800ba69c68277430fe22987f44dc484ea174ebf0f2eff58b3dd96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:3-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:bfafe8f3bb4837f6c953407d230673a7d9e1ac62090dd2d2958a76c7ee7bf9aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110950046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7a5df16817c92db5afa216b5c83fa2ce270e345f5036a7d45ae10a91ee92e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 13 Oct 2021 05:53:13 GMT
ENV NODE_VERSION=12.22.7
# Wed, 13 Oct 2021 05:53:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c8672a664087e96b4e2804caf77a0aaa8c1375ae6b378edb220a678155383a81"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 13 Oct 2021 05:53:21 GMT
ENV YARN_VERSION=1.22.15
# Wed, 13 Oct 2021 05:53:25 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 22 Oct 2021 18:56:08 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:56:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Oct 2021 18:56:09 GMT
CMD ["node"]
# Fri, 22 Oct 2021 21:06:58 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 22 Oct 2021 21:06:59 GMT
RUN apk add --no-cache 		bash
# Fri, 22 Oct 2021 21:06:59 GMT
ENV NODE_ENV=production
# Fri, 22 Oct 2021 21:06:59 GMT
ENV GHOST_CLI_VERSION=1.17.4
# Fri, 22 Oct 2021 21:07:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Oct 2021 21:07:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Oct 2021 21:07:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Oct 2021 21:07:23 GMT
ENV GHOST_VERSION=3.42.6
# Fri, 22 Oct 2021 21:08:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Oct 2021 21:08:37 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Oct 2021 21:08:37 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Oct 2021 21:08:37 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Oct 2021 21:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Oct 2021 21:08:38 GMT
EXPOSE 2368
# Fri, 22 Oct 2021 21:08:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a283ce1b66428fc93c65408c0128579557a02034be3bbacdbb3134e69cb44b`  
		Last Modified: Wed, 13 Oct 2021 06:11:17 GMT  
		Size: 24.7 MB (24743708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac04d48e2d0fdff51b2fb0790cb5de894ca75a316816975df7e8cc0207d5af`  
		Last Modified: Wed, 13 Oct 2021 06:11:11 GMT  
		Size: 2.4 MB (2366327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d519dd2164e02bf751c50c929299851e5274522c593856df9dd0b15545801237`  
		Last Modified: Fri, 22 Oct 2021 19:10:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2f01b981afdedd1ae3c1129499fe93df38fcf0ab7c1514a9025d352f00c510`  
		Last Modified: Fri, 22 Oct 2021 21:10:28 GMT  
		Size: 10.1 KB (10067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daa8cd454386962228d6e4f7c96f9d2a64412d51ba683d677422e050c12224b`  
		Last Modified: Fri, 22 Oct 2021 21:10:29 GMT  
		Size: 779.6 KB (779621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18563b1cfb6df41ea7006a370925874d8c1196bbf73b4564f8eafddd3acb1814`  
		Last Modified: Fri, 22 Oct 2021 21:10:31 GMT  
		Size: 9.4 MB (9425113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d718751aa5167cefa26c86f5d0c232a87ef87a6cb1703d91a191d73c503659`  
		Last Modified: Fri, 22 Oct 2021 21:10:44 GMT  
		Size: 70.8 MB (70822501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefe125caab044f5080504a8b770734648df644d0c6f6c492a8898ecf03bb086`  
		Last Modified: Fri, 22 Oct 2021 21:10:28 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:1009db8a2c3d442d1e15addc74a05d9a3f86e1123a703ca7f0eebc7da8b458a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94903363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116f6f47b9ffe8f3836988e40521952bace1e5166ad78caad51affdbe8c6acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:45 GMT
ADD file:6b70601c3d32558ee0cefe87b44ce4c4c8e85db5211f940538f9acf03f6ba6be in / 
# Tue, 31 Aug 2021 22:30:45 GMT
CMD ["/bin/sh"]
# Wed, 13 Oct 2021 04:44:55 GMT
ENV NODE_VERSION=12.22.7
# Wed, 13 Oct 2021 05:01:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c8672a664087e96b4e2804caf77a0aaa8c1375ae6b378edb220a678155383a81"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 13 Oct 2021 05:01:30 GMT
ENV YARN_VERSION=1.22.15
# Wed, 13 Oct 2021 05:01:39 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 22 Oct 2021 17:53:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Oct 2021 17:53:22 GMT
CMD ["node"]
# Fri, 22 Oct 2021 19:13:36 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 22 Oct 2021 19:13:38 GMT
RUN apk add --no-cache 		bash
# Fri, 22 Oct 2021 19:13:39 GMT
ENV NODE_ENV=production
# Fri, 22 Oct 2021 19:13:39 GMT
ENV GHOST_CLI_VERSION=1.17.4
# Fri, 22 Oct 2021 19:14:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Oct 2021 19:14:51 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Oct 2021 19:14:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Oct 2021 19:14:52 GMT
ENV GHOST_VERSION=3.42.6
# Fri, 22 Oct 2021 19:23:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Oct 2021 19:23:46 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Oct 2021 19:23:47 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Oct 2021 19:23:48 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Oct 2021 19:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Oct 2021 19:23:49 GMT
EXPOSE 2368
# Fri, 22 Oct 2021 19:23:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b3e69bfc382676dcc8e89f289815a72b60fdf61e66e21d90b8851cbb4b5e3aeb`  
		Last Modified: Tue, 31 Aug 2021 22:32:25 GMT  
		Size: 2.6 MB (2606586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249ee21de92da0c71c6e4ef63291e5319183995a520d22545c7cdedf38adefd6`  
		Last Modified: Wed, 13 Oct 2021 05:48:43 GMT  
		Size: 24.2 MB (24171950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bdc130a4a0d4abd36fc6b0fa9a04932014445794a4aa1a06dd8bf8a8d269ff`  
		Last Modified: Wed, 13 Oct 2021 05:48:29 GMT  
		Size: 2.4 MB (2417727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4ffee52cd55e4b79cd7e8e4829035421c97718681e0410a55ae47c3d519f8a`  
		Last Modified: Fri, 22 Oct 2021 18:05:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcfd76baeeedceaf27649d7fe5f4b88ee322d080e8f0e977ab89bc920455c38`  
		Last Modified: Fri, 22 Oct 2021 19:24:17 GMT  
		Size: 9.9 KB (9905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0719337e39fa489eb0d7163e62f38013e72e05a4cd4574b8539941e80fe73112`  
		Last Modified: Fri, 22 Oct 2021 19:24:17 GMT  
		Size: 734.0 KB (734011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89fdbbc22321ac053bc84f2c960c35c22ce9ad48696a38ee80f541866aeb4bf`  
		Last Modified: Fri, 22 Oct 2021 19:24:31 GMT  
		Size: 9.4 MB (9425787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337f1400caa49d9af5e6813ecb44642d548a8e9f81b99517b5ca72f9536552e2`  
		Last Modified: Fri, 22 Oct 2021 19:25:31 GMT  
		Size: 55.5 MB (55536402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88ba4997a04a43885eeac71ed45b3a649309b6dd01e77602b2a2725231dc48e`  
		Last Modified: Fri, 22 Oct 2021 19:24:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:fff04788576051be289cffad7cc2d8fd6acd56f652c0f345711fdd9b811979c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93699508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbb16997db84f98f5f9ece985e16339b72845c43a36f5df3c816710207b4601`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 01 Sep 2021 01:27:09 GMT
ADD file:fb3ea1e5df00e24345fc4f1adf07702f4ec457a6f7249f6ad06c72e2570955a0 in / 
# Wed, 01 Sep 2021 01:27:10 GMT
CMD ["/bin/sh"]
# Wed, 13 Oct 2021 04:54:16 GMT
ENV NODE_VERSION=12.22.7
# Wed, 13 Oct 2021 05:08:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c8672a664087e96b4e2804caf77a0aaa8c1375ae6b378edb220a678155383a81"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 13 Oct 2021 05:08:54 GMT
ENV YARN_VERSION=1.22.15
# Wed, 13 Oct 2021 05:09:04 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 13 Oct 2021 05:09:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 13 Oct 2021 05:09:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 05:09:07 GMT
CMD ["node"]
# Wed, 13 Oct 2021 08:03:19 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Oct 2021 08:03:21 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Oct 2021 08:03:21 GMT
ENV NODE_ENV=production
# Mon, 18 Oct 2021 22:29:58 GMT
ENV GHOST_CLI_VERSION=1.17.4
# Mon, 18 Oct 2021 22:30:48 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 18 Oct 2021 22:30:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 18 Oct 2021 22:30:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 18 Oct 2021 22:30:51 GMT
ENV GHOST_VERSION=3.42.6
# Mon, 18 Oct 2021 22:37:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 18 Oct 2021 22:37:29 GMT
WORKDIR /var/lib/ghost
# Mon, 18 Oct 2021 22:37:29 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 18 Oct 2021 22:37:30 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 18 Oct 2021 22:37:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:37:31 GMT
EXPOSE 2368
# Mon, 18 Oct 2021 22:37:31 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b3b5e25c4f507c4fe7952504ebbc679023d8699d9c6b2b61376ed676d1ab572`  
		Last Modified: Wed, 01 Sep 2021 01:28:52 GMT  
		Size: 2.4 MB (2410387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee9975198d53b55f180570322cb4700ad44eebb1869df2fda6e976f7525171b`  
		Last Modified: Wed, 13 Oct 2021 06:23:50 GMT  
		Size: 23.7 MB (23728530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9e0182fa8af29c09345b5f0476d74f2044754a5dee403a5acf4c46df2e3ccf`  
		Last Modified: Wed, 13 Oct 2021 06:23:34 GMT  
		Size: 2.4 MB (2417833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b93da904177047162244ad26876fa622e3c82478b2b67a9bee5e4e33bf66a`  
		Last Modified: Wed, 13 Oct 2021 06:23:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642f1e12cc7c5575f7b1d8b6332780e6e6ea59943fd06bb957adab52aa918246`  
		Last Modified: Wed, 13 Oct 2021 08:14:54 GMT  
		Size: 9.7 KB (9694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3764f6aa8fc414a4e49790f098c8ccc9475a53f6837fef764047f0fc1268e03a`  
		Last Modified: Wed, 13 Oct 2021 08:14:55 GMT  
		Size: 671.2 KB (671152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb436c12b32ef6f919b27230a8530206931c5c756b7e55da7e598d444bbd518`  
		Last Modified: Mon, 18 Oct 2021 22:41:51 GMT  
		Size: 9.4 MB (9425401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc6f85ed8980dc82fe56c777bdefeacd00ba3af045b8293b3f63007ce4bd6`  
		Last Modified: Mon, 18 Oct 2021 22:42:50 GMT  
		Size: 55.0 MB (55035684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d079b1d7b0b403e4b41966b1647b3553469016f0bf1b6a1f11820392472b3cff`  
		Last Modified: Mon, 18 Oct 2021 22:41:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:824ee7789e4e3b01df08d17e5623a6cdc33b69a7c9c626b1899216285b1b3de9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95970064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af470be8ed27972e680114010a188a23fd317f508055266cfcf6e2c5be85481a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:52 GMT
ADD file:065608b23c19f03e2753bacf8f548d77f05519f94648c6872303aa1d1fc9254b in / 
# Wed, 01 Sep 2021 02:50:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Oct 2021 04:21:14 GMT
ENV NODE_VERSION=12.22.7
# Wed, 13 Oct 2021 04:36:47 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c8672a664087e96b4e2804caf77a0aaa8c1375ae6b378edb220a678155383a81"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 13 Oct 2021 04:36:47 GMT
ENV YARN_VERSION=1.22.15
# Wed, 13 Oct 2021 04:36:53 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Fri, 22 Oct 2021 17:48:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Oct 2021 17:48:40 GMT
CMD ["node"]
# Fri, 22 Oct 2021 19:36:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 22 Oct 2021 19:36:52 GMT
RUN apk add --no-cache 		bash
# Fri, 22 Oct 2021 19:36:53 GMT
ENV NODE_ENV=production
# Fri, 22 Oct 2021 19:36:54 GMT
ENV GHOST_CLI_VERSION=1.17.4
# Fri, 22 Oct 2021 19:37:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 22 Oct 2021 19:37:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 22 Oct 2021 19:37:18 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 22 Oct 2021 19:37:19 GMT
ENV GHOST_VERSION=3.42.6
# Fri, 22 Oct 2021 19:40:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Fri, 22 Oct 2021 19:40:20 GMT
WORKDIR /var/lib/ghost
# Fri, 22 Oct 2021 19:40:23 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 22 Oct 2021 19:40:26 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Fri, 22 Oct 2021 19:40:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Oct 2021 19:40:32 GMT
EXPOSE 2368
# Fri, 22 Oct 2021 19:40:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ccdebe76d52933c5fff4a8db8870e8454f3dc3c92a88e59acc5eb30c6c1178af`  
		Last Modified: Wed, 01 Sep 2021 02:51:48 GMT  
		Size: 2.7 MB (2712295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3104f9b149b8d186678633bfd0f564186c5a83e0da6f0079f37cc2851471202`  
		Last Modified: Wed, 13 Oct 2021 05:30:14 GMT  
		Size: 24.9 MB (24884702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82758d53ab1ccd1f56efccc104500d3919cc74c4dfd13b826ccd7f77dad39ca4`  
		Last Modified: Wed, 13 Oct 2021 05:30:10 GMT  
		Size: 2.4 MB (2425035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1693df6fd0321db72802024b0a59b00e58f989f56b83db152a92afb58659cf`  
		Last Modified: Fri, 22 Oct 2021 18:07:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebefd3615bd21de0dc3ccc7c45357acdc065bcdeb19793104b4a1662b0038e16`  
		Last Modified: Fri, 22 Oct 2021 19:42:06 GMT  
		Size: 9.9 KB (9932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15edb59fce33a3ab09477d79786a6ca4b5035170ca3d0fd46d399eae229fa83`  
		Last Modified: Fri, 22 Oct 2021 19:42:07 GMT  
		Size: 791.5 KB (791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a7e0821984615dc8366744f5a4d185c686697fc68017c452b8167f2461364`  
		Last Modified: Fri, 22 Oct 2021 19:42:09 GMT  
		Size: 9.4 MB (9425020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee08bc89384fe17f53a35e54a506e2133b2fd467e453cd664d4d6b85acc5a8`  
		Last Modified: Fri, 22 Oct 2021 19:42:21 GMT  
		Size: 55.7 MB (55720578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e649371079fb049057ef957d699a0ae6b3309d7c0329267344f2c8aaee3047e`  
		Last Modified: Fri, 22 Oct 2021 19:42:06 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

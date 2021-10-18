## `ghost:3-alpine`

```console
$ docker pull ghost@sha256:febc0ad28c8d7190b7de97796658382c2ff80271d792bd7c1faba774e15eae18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:3-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:f9e7a98c8b87dc3c9a5fc94fdb4f4bc06547ff7ffe5a58568c38c6c150fa55c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c53a1e8e19187bef2742ac951627a952024ba8833509f7d08017c9802e5aea7`
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
# Wed, 13 Oct 2021 05:53:25 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 13 Oct 2021 05:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 05:53:26 GMT
CMD ["node"]
# Wed, 13 Oct 2021 16:25:22 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Oct 2021 16:25:23 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Oct 2021 16:25:23 GMT
ENV NODE_ENV=production
# Mon, 18 Oct 2021 21:25:42 GMT
ENV GHOST_CLI_VERSION=1.17.4
# Mon, 18 Oct 2021 21:26:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 18 Oct 2021 21:26:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 18 Oct 2021 21:26:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 18 Oct 2021 21:26:05 GMT
ENV GHOST_VERSION=3.42.6
# Mon, 18 Oct 2021 21:27:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 18 Oct 2021 21:27:14 GMT
WORKDIR /var/lib/ghost
# Mon, 18 Oct 2021 21:27:14 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 18 Oct 2021 21:27:15 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 18 Oct 2021 21:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:27:15 GMT
EXPOSE 2368
# Mon, 18 Oct 2021 21:27:15 GMT
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
	-	`sha256:5c0c71da08f4fbfaa5054c14154a84b25fd8cb4405bf136f859d62af92b30a2a`  
		Last Modified: Wed, 13 Oct 2021 06:11:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575e9dd567470a717d946f75b303edd3a004c2fcfcb407db36507feea34a5459`  
		Last Modified: Wed, 13 Oct 2021 16:28:36 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08034ade4d38a48be69e6a5918cc1aac4ab9a0b843d597af1bc7094bf5c73687`  
		Last Modified: Wed, 13 Oct 2021 16:28:36 GMT  
		Size: 779.6 KB (779621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5898b95c516d19e65cc3e8a5160f889fb6438205422055db678f822a84024d0`  
		Last Modified: Mon, 18 Oct 2021 21:28:57 GMT  
		Size: 9.4 MB (9425179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d028882e8cd1d09ae15771fdc28b117595d00177b86b34bd9b0e4ef9ea1fbb42`  
		Last Modified: Mon, 18 Oct 2021 21:29:08 GMT  
		Size: 70.8 MB (70826607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a796d6354d2a0a8160f3641ae55bacf1f2e04985103797c972fc815a603e1639`  
		Last Modified: Mon, 18 Oct 2021 21:28:54 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:418a3bff96af80ae8192bd9dee7de7d3c354ae2df53e755da64dd4d6950d0de9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94867318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833476e5c5917f11aa8f10dedd8cdf09b4746808f586583d9a81ea78007f4271`
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
# Wed, 13 Oct 2021 05:01:40 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 13 Oct 2021 05:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 05:01:41 GMT
CMD ["node"]
# Wed, 13 Oct 2021 06:25:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Oct 2021 06:25:37 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Oct 2021 06:25:37 GMT
ENV NODE_ENV=production
# Wed, 13 Oct 2021 06:25:37 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Wed, 13 Oct 2021 06:26:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 13 Oct 2021 06:26:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Oct 2021 06:26:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Oct 2021 06:26:47 GMT
ENV GHOST_VERSION=3.42.6
# Wed, 13 Oct 2021 06:35:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 13 Oct 2021 06:35:33 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Oct 2021 06:35:33 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Oct 2021 06:35:34 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 13 Oct 2021 06:35:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:35:35 GMT
EXPOSE 2368
# Wed, 13 Oct 2021 06:35:35 GMT
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
	-	`sha256:9b082ea6031caeab8b0cd407cefeca85c7e32dade3d02c7f26b246c31e8051be`  
		Last Modified: Wed, 13 Oct 2021 05:48:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4feb58c38d4e706f21329d9a788861453474377058e18b02735f788cbdc56c`  
		Last Modified: Wed, 13 Oct 2021 06:36:01 GMT  
		Size: 9.9 KB (9901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf14702f30e98fc373978d34fc0791cbd471d1cf3756de69f2d396bdde9809`  
		Last Modified: Wed, 13 Oct 2021 06:36:01 GMT  
		Size: 734.0 KB (734020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7deaf3a5c4c5606ba3f92a55a369029b9b62df041fe4d641364e5aa9cc670c2`  
		Last Modified: Wed, 13 Oct 2021 06:36:15 GMT  
		Size: 9.4 MB (9391117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61c0e758fd05936932bb35f504491cb0122302d2afe3fa847b6c95203f6837`  
		Last Modified: Wed, 13 Oct 2021 06:37:15 GMT  
		Size: 55.5 MB (55535189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8219de3a43b1245275613881fe4dee759947e696f8ab557e0934f4424f6d085`  
		Last Modified: Wed, 13 Oct 2021 06:36:01 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:9ff0764934f3024a9121acab8d32298d6a942a67f85b83e2ed6c2dcae6f9e0b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93664505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048cc31ebdef4016cfab68835e5f0d74148fd0d4397699d22e01acbaaf36b2ad`
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
# Wed, 13 Oct 2021 08:03:22 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Wed, 13 Oct 2021 08:04:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 13 Oct 2021 08:04:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Oct 2021 08:04:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Oct 2021 08:04:11 GMT
ENV GHOST_VERSION=3.42.6
# Wed, 13 Oct 2021 08:10:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 13 Oct 2021 08:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Oct 2021 08:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Oct 2021 08:10:51 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 13 Oct 2021 08:10:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 08:10:52 GMT
EXPOSE 2368
# Wed, 13 Oct 2021 08:10:52 GMT
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
	-	`sha256:0a68d1c785392d378586b3047f8b594b395ce01d25997a6ee21b04063914b8c2`  
		Last Modified: Wed, 13 Oct 2021 08:15:10 GMT  
		Size: 9.4 MB (9390706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f1fba15c6059300e5caedc941f3c1a93bbfb5464435ac4aa13a910c023ac95`  
		Last Modified: Wed, 13 Oct 2021 08:16:08 GMT  
		Size: 55.0 MB (55035378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567094a1590564da8189d9b2fda899a541442305814604259f8adca40484b44`  
		Last Modified: Wed, 13 Oct 2021 08:14:54 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:10085674713a4040374b277c6c9dd90765c074009682b1723bdac088d744728a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95967617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650fa843fdc6b9a6772ea8a297f6e253bcf7c07c06a111debc99b3c88ecba706`
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
# Wed, 13 Oct 2021 04:36:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 13 Oct 2021 04:36:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 04:36:55 GMT
CMD ["node"]
# Wed, 13 Oct 2021 05:50:21 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Oct 2021 05:50:22 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Oct 2021 05:50:23 GMT
ENV NODE_ENV=production
# Mon, 18 Oct 2021 22:00:28 GMT
ENV GHOST_CLI_VERSION=1.17.4
# Mon, 18 Oct 2021 22:00:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 18 Oct 2021 22:00:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 18 Oct 2021 22:00:51 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 18 Oct 2021 22:00:52 GMT
ENV GHOST_VERSION=3.42.6
# Mon, 18 Oct 2021 22:03:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 18 Oct 2021 22:03:56 GMT
WORKDIR /var/lib/ghost
# Mon, 18 Oct 2021 22:03:59 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 18 Oct 2021 22:04:02 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 18 Oct 2021 22:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:04:07 GMT
EXPOSE 2368
# Mon, 18 Oct 2021 22:04:10 GMT
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
	-	`sha256:d338ed46a7095a1f092705dd63235ff7152dd5c0b9d7d5352f1beab859d2ae12`  
		Last Modified: Wed, 13 Oct 2021 05:30:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2468fd025e5a0e72b123e96f59e551cdc64a95bd72e6811c98304a3e41c4a792`  
		Last Modified: Wed, 13 Oct 2021 05:55:22 GMT  
		Size: 9.9 KB (9929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb31ec2d9f3d1a1ddc23556f4e0caf7006f03d0bc255b9eb61ee51d04c3a18`  
		Last Modified: Wed, 13 Oct 2021 05:55:22 GMT  
		Size: 791.5 KB (791510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b78b5299bd2bf58ad3a5ab9524e1292cf07f714b61db0e8227a75407306e6c1`  
		Last Modified: Mon, 18 Oct 2021 22:05:45 GMT  
		Size: 9.4 MB (9425004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd37278d87f0406c90b6d2f4454fbaba924a1b7b14b74f5e10a69ff5c8d2220`  
		Last Modified: Mon, 18 Oct 2021 22:05:56 GMT  
		Size: 55.7 MB (55718316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfa99047485a7ca31e2661ef047a6791f35afe93fdde2cb0f1e6fc584743f95`  
		Last Modified: Mon, 18 Oct 2021 22:05:42 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

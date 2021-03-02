## `ghost:2-alpine`

```console
$ docker pull ghost@sha256:b8ff2384425f43c010fd9c7d4fa0821349f34ebfab2f8b3de6b79a7fe784ffa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ghost:2-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:382feafef2563162faf8f1df96df4c4455db64b1a714406f5fee32b9457dd310
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107615647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9a65c10c6ad2dc22a91ccb594f1bc8d057c35f5c4ac49cd8b8d87c6294e8de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:08:47 GMT
ENV NODE_VERSION=10.24.0
# Wed, 24 Feb 2021 21:08:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 24 Feb 2021 21:08:57 GMT
ENV YARN_VERSION=1.22.5
# Wed, 24 Feb 2021 21:09:01 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 24 Feb 2021 21:09:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:09:02 GMT
CMD ["node"]
# Thu, 25 Feb 2021 03:42:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 25 Feb 2021 03:42:55 GMT
RUN apk add --no-cache 		bash
# Thu, 25 Feb 2021 03:42:55 GMT
ENV NODE_ENV=production
# Mon, 01 Mar 2021 23:31:04 GMT
ENV GHOST_CLI_VERSION=1.16.0
# Mon, 01 Mar 2021 23:31:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 01 Mar 2021 23:31:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 01 Mar 2021 23:31:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 01 Mar 2021 23:31:26 GMT
ENV GHOST_VERSION=2.38.3
# Mon, 01 Mar 2021 23:32:20 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 01 Mar 2021 23:32:20 GMT
WORKDIR /var/lib/ghost
# Mon, 01 Mar 2021 23:32:20 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 01 Mar 2021 23:32:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 01 Mar 2021 23:32:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Mar 2021 23:32:21 GMT
EXPOSE 2368
# Mon, 01 Mar 2021 23:32:21 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eba68f0dd912539668bd3fa6f024e36ca2805434cf4191bed73617d7666fb45`  
		Last Modified: Wed, 24 Feb 2021 21:16:05 GMT  
		Size: 22.2 MB (22205106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457d8b37e078bc9333cdd742e4c6f87a4b8b38628b27e4e90d7f3ff1b35102a2`  
		Last Modified: Wed, 24 Feb 2021 21:15:59 GMT  
		Size: 2.3 MB (2344619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb74c73c5777d1912e80b7dec9cc2cd28d024be4cb4de6f5f1d4752fa1f8c5d`  
		Last Modified: Wed, 24 Feb 2021 21:15:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d794c846cbabb7dca3c22097c2feebe5dc6dc8f8c865379096b0a467688f5`  
		Last Modified: Thu, 25 Feb 2021 03:45:00 GMT  
		Size: 9.9 KB (9907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776af5d70aaf9a885c6f5aafa2e804ce800bfe40662373b55bc17303bfd938db`  
		Last Modified: Thu, 25 Feb 2021 03:45:00 GMT  
		Size: 780.5 KB (780519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8feea6666da32ba573133c811bd1587d8b60999c9b61ac62eabc8d44b611c112`  
		Last Modified: Mon, 01 Mar 2021 23:34:03 GMT  
		Size: 7.4 MB (7391697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49bf807530b799f6e30e218ddbf1745a9f217bfc85eb947b2684e2b1bb8899e`  
		Last Modified: Mon, 01 Mar 2021 23:34:12 GMT  
		Size: 72.1 MB (72067659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27e9aa763f8518ebb14ee7d7555f6e2ca333be266ecb4d994d46e3462d8fe33`  
		Last Modified: Mon, 01 Mar 2021 23:34:00 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:32dc2139a5929ea7e9fd1540b0673c276f76170dc432c1b4f3175879f0ec94ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92169835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38c0abb1473a7e356b44eebe60676b897e1fc2d58e33a46e9cd0a52f638e802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:26:55 GMT
ENV NODE_VERSION=10.24.0
# Thu, 25 Feb 2021 02:33:12 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 25 Feb 2021 02:33:15 GMT
ENV YARN_VERSION=1.22.5
# Thu, 25 Feb 2021 02:33:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 25 Feb 2021 02:33:22 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 25 Feb 2021 02:33:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Feb 2021 02:33:24 GMT
CMD ["node"]
# Thu, 25 Feb 2021 04:10:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 25 Feb 2021 04:10:37 GMT
RUN apk add --no-cache 		bash
# Thu, 25 Feb 2021 04:10:38 GMT
ENV NODE_ENV=production
# Tue, 02 Mar 2021 00:01:30 GMT
ENV GHOST_CLI_VERSION=1.16.0
# Tue, 02 Mar 2021 00:02:18 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 02 Mar 2021 00:02:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 02 Mar 2021 00:02:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 02 Mar 2021 00:02:24 GMT
ENV GHOST_VERSION=2.38.3
# Tue, 02 Mar 2021 00:08:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 02 Mar 2021 00:08:39 GMT
WORKDIR /var/lib/ghost
# Tue, 02 Mar 2021 00:08:41 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 02 Mar 2021 00:08:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 02 Mar 2021 00:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 00:08:44 GMT
EXPOSE 2368
# Tue, 02 Mar 2021 00:08:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3c6a1b1ce6829a51de244a7fb43d44ef801d80e555580d9f9767ac32c1adc0`  
		Last Modified: Thu, 25 Feb 2021 02:39:12 GMT  
		Size: 21.6 MB (21646153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5028d8930eb3b35d4fe44a75745053006a4fa2f7c5ed3a930d97f6b0c5671046`  
		Last Modified: Thu, 25 Feb 2021 02:39:04 GMT  
		Size: 2.4 MB (2368067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27f01eeb3febdf3c3f5451fe261033afe5aa78e23fc9cba4ee209aff3bb4b1`  
		Last Modified: Thu, 25 Feb 2021 02:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa552b010d6111574aedd262e178a338a0145f02ebccbb2cfe8730b66b159e46`  
		Last Modified: Thu, 25 Feb 2021 04:18:20 GMT  
		Size: 9.7 KB (9734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc87dd5a3d923cae99cd07431398bf3012f730d530b769c8c5e2e0d773676`  
		Last Modified: Thu, 25 Feb 2021 04:18:20 GMT  
		Size: 733.5 KB (733468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53f1475af4d89e167e8b3950ba0be7f4d9bc849d9df849434e701ad17c0df0d`  
		Last Modified: Tue, 02 Mar 2021 00:09:55 GMT  
		Size: 7.4 MB (7391531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efd9a710b99b910af984ed92f52e83cd41faea9d0d052ed852c96b0a17ce060`  
		Last Modified: Tue, 02 Mar 2021 00:10:15 GMT  
		Size: 57.4 MB (57398988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a5205a46e10204da20cae11a77f764bd39fcc1c27bd71fa6abcd83486d1234`  
		Last Modified: Tue, 02 Mar 2021 00:09:50 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:516551959d96cd7e7fdd74320413a8524cb9315dd5898adabc71785a6f995099
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91071249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc095e08f746a05895003153f7c6114eb6c07f3d67b5e7a55bf8c5cfc4fbc5f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Feb 2021 21:03:48 GMT
ADD file:82e5f31ae641a6461af880d0c7542790da0501aece98e2bb53441943dc92bd1c in / 
# Wed, 24 Feb 2021 21:03:49 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 00:18:54 GMT
ENV NODE_VERSION=10.24.0
# Thu, 25 Feb 2021 00:23:52 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 25 Feb 2021 00:23:56 GMT
ENV YARN_VERSION=1.22.5
# Thu, 25 Feb 2021 00:24:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 25 Feb 2021 00:24:06 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 25 Feb 2021 00:24:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Feb 2021 00:24:08 GMT
CMD ["node"]
# Thu, 25 Feb 2021 02:54:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 25 Feb 2021 02:54:28 GMT
RUN apk add --no-cache 		bash
# Thu, 25 Feb 2021 02:54:29 GMT
ENV NODE_ENV=production
# Thu, 25 Feb 2021 02:54:29 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Thu, 25 Feb 2021 02:55:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 25 Feb 2021 02:55:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 25 Feb 2021 02:55:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 25 Feb 2021 02:55:08 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 25 Feb 2021 02:59:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 25 Feb 2021 02:59:38 GMT
WORKDIR /var/lib/ghost
# Thu, 25 Feb 2021 02:59:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 25 Feb 2021 02:59:39 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 25 Feb 2021 02:59:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Feb 2021 02:59:41 GMT
EXPOSE 2368
# Thu, 25 Feb 2021 02:59:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1a3a062e2a467af6eb6c2a8701b748dbda4bfa88ea0a3c2901d72015da721a72`  
		Last Modified: Wed, 24 Feb 2021 21:04:31 GMT  
		Size: 2.4 MB (2423575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60007d4dbc28613bee495c17731659942821ae1ef51588802f6e0d8b96dc903`  
		Last Modified: Thu, 25 Feb 2021 00:35:31 GMT  
		Size: 21.2 MB (21246599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f9c0e18f56e90d0901854780d4cdca80ae15f7b103582807823852309ce2e4`  
		Last Modified: Thu, 25 Feb 2021 00:35:23 GMT  
		Size: 2.4 MB (2368164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd4bcf8750ad6155acc46d0284647632108cf4d6d4c5fbb38fae7b7a4d838f2`  
		Last Modified: Thu, 25 Feb 2021 00:35:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398e7c43f1e8df6dad8a6cce5a46f1a1a1ec817e0d4034e19a0e3f1a5fa19f5`  
		Last Modified: Thu, 25 Feb 2021 03:01:13 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b049e631e714ef4f10cc3c070c10cb09140a2b8bad82fc7c12a18f1e1051b2`  
		Last Modified: Thu, 25 Feb 2021 03:01:13 GMT  
		Size: 669.0 KB (669034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229498ac60c7dca03d209e51b3ef2324d3e465982ea5638061c3be591d7a788e`  
		Last Modified: Thu, 25 Feb 2021 03:01:16 GMT  
		Size: 7.4 MB (7439122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7598a0454c686244f97305031d0d0d861fa159f135589f585810fc5c30d99633`  
		Last Modified: Thu, 25 Feb 2021 03:01:36 GMT  
		Size: 56.9 MB (56914408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96957debac0751f924731b922dc9bb990be15b30701fbfe7c83cc40c6c539c48`  
		Last Modified: Thu, 25 Feb 2021 03:01:13 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:dd45fea72489e771f1b6a5c88b3f468d207a2f97fa8ca1702ef18fad5552f0e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93370178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10e103ca1f9523f7b18bdc229c8549580522cec25795e0f5508ee591aed2b85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 01:54:41 GMT
ENV NODE_VERSION=10.24.0
# Thu, 25 Feb 2021 02:01:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 25 Feb 2021 02:01:46 GMT
ENV YARN_VERSION=1.22.5
# Thu, 25 Feb 2021 02:01:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 25 Feb 2021 02:01:58 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 25 Feb 2021 02:01:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Feb 2021 02:02:00 GMT
CMD ["node"]
# Thu, 25 Feb 2021 05:17:12 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 25 Feb 2021 05:17:14 GMT
RUN apk add --no-cache 		bash
# Thu, 25 Feb 2021 05:17:15 GMT
ENV NODE_ENV=production
# Thu, 25 Feb 2021 05:17:16 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Thu, 25 Feb 2021 05:17:43 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 25 Feb 2021 05:17:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 25 Feb 2021 05:17:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 25 Feb 2021 05:17:47 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 25 Feb 2021 05:22:03 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 25 Feb 2021 05:22:10 GMT
WORKDIR /var/lib/ghost
# Thu, 25 Feb 2021 05:22:11 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 25 Feb 2021 05:22:12 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 25 Feb 2021 05:22:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Feb 2021 05:22:13 GMT
EXPOSE 2368
# Thu, 25 Feb 2021 05:22:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e09cdaf6556f32898f34fbfcf4ef1d70d68bc02b476c81bfd60d5bf47846b6`  
		Last Modified: Thu, 25 Feb 2021 02:10:38 GMT  
		Size: 22.5 MB (22464075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cb308f22514a2b0742fc965d83360a86fcf13071b23c35b036ac8b36ff2bc`  
		Last Modified: Thu, 25 Feb 2021 02:10:32 GMT  
		Size: 2.4 MB (2408216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd662c8c68ec7810b5edcac87b298e28c0e04ff1450abe0612aa6845f9d51c7`  
		Last Modified: Thu, 25 Feb 2021 02:10:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5610c2e3ab30b95058ec15e616095a777d6c19338b36e8957c135bfbf68dd77f`  
		Last Modified: Thu, 25 Feb 2021 05:23:29 GMT  
		Size: 9.9 KB (9852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b920c4fa1cfd2d1585eb692759aeb7e520430eaaf907988a95a753601a1ea8c`  
		Last Modified: Thu, 25 Feb 2021 05:23:29 GMT  
		Size: 792.1 KB (792137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543eb64871f34f88b9aaaa2befcde2ee2ae66aa8e2ff1b7e32e51f16c680cba6`  
		Last Modified: Thu, 25 Feb 2021 05:23:33 GMT  
		Size: 7.4 MB (7438648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889fdab773adb54d04c1192d62d252692f9656c0b7daae50fadf5b012bca3df`  
		Last Modified: Thu, 25 Feb 2021 05:23:51 GMT  
		Size: 57.5 MB (57530606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae306ff3e2252c67123a3069195d8680dfc64554efc3c502676bbbd37b711fd0`  
		Last Modified: Thu, 25 Feb 2021 05:23:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; 386

```console
$ docker pull ghost@sha256:5135ed2b03456443dae1057e2de5e00f9586563e8473002b97632fcb8dc9545a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93510735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51673d1564ebe737e1350f669125d6271579c45c4e9541e83a0bfba40a937894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:50 GMT
ADD file:64fc1c8d8fc09e72c022bd1f32d6c91f477c86a094091c52866e974be309397c in / 
# Wed, 24 Feb 2021 20:38:50 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:43:59 GMT
ENV NODE_VERSION=10.24.0
# Wed, 24 Feb 2021 23:29:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 24 Feb 2021 23:29:37 GMT
ENV YARN_VERSION=1.22.5
# Wed, 24 Feb 2021 23:29:41 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 24 Feb 2021 23:29:41 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 24 Feb 2021 23:29:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:29:42 GMT
CMD ["node"]
# Thu, 25 Feb 2021 02:30:19 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 25 Feb 2021 02:30:21 GMT
RUN apk add --no-cache 		bash
# Thu, 25 Feb 2021 02:30:21 GMT
ENV NODE_ENV=production
# Mon, 01 Mar 2021 23:38:34 GMT
ENV GHOST_CLI_VERSION=1.16.0
# Mon, 01 Mar 2021 23:38:57 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 01 Mar 2021 23:38:58 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 01 Mar 2021 23:38:58 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 01 Mar 2021 23:38:58 GMT
ENV GHOST_VERSION=2.38.3
# Mon, 01 Mar 2021 23:43:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 01 Mar 2021 23:43:08 GMT
WORKDIR /var/lib/ghost
# Mon, 01 Mar 2021 23:43:08 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 01 Mar 2021 23:43:09 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 01 Mar 2021 23:43:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Mar 2021 23:43:09 GMT
EXPOSE 2368
# Mon, 01 Mar 2021 23:43:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9051e839b1b135f9f278b020eff90cafb103216d09b63d7aa3dde15fbade3c6a`  
		Last Modified: Wed, 24 Feb 2021 20:39:32 GMT  
		Size: 2.8 MB (2810924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df97db544d72bd596a3021fa1f4581ad3c1fcc1095e3787f9366019fbf8fecda`  
		Last Modified: Wed, 24 Feb 2021 23:30:37 GMT  
		Size: 22.4 MB (22440112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae1cc5606c6d91fac3aa2a2701c60c6fed74bb77b6f33ea2f57cd9777f0d9a5`  
		Last Modified: Wed, 24 Feb 2021 23:30:30 GMT  
		Size: 2.4 MB (2368167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ada93971748097e4a721cb0bea44ee7cdde6af9adc7fe7570c22a7a0835ab09`  
		Last Modified: Wed, 24 Feb 2021 23:30:29 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00864d39d86eb3a689e1cb9f485784049a894ad6a88c35cfaa4a22d2fbdc65cc`  
		Last Modified: Thu, 25 Feb 2021 02:34:29 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f278711100fc3e2ed1a4a3defb6b2c9012c94ccfbca220a0518fd654daf8b6`  
		Last Modified: Thu, 25 Feb 2021 02:34:29 GMT  
		Size: 831.1 KB (831095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd568aa1a571b559192f924c661ace9d3c5a9d13cb246006cf5299402ae49c2a`  
		Last Modified: Mon, 01 Mar 2021 23:43:37 GMT  
		Size: 7.4 MB (7391662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d4c6638ab40c5db2c10bd254f8317a4a279d1bed68350ed5d3aa33b9a88d1a`  
		Last Modified: Mon, 01 Mar 2021 23:43:55 GMT  
		Size: 57.7 MB (57657967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8fea4c9b14addaf5276d37630afc320959238510ecdc1a45234cc2e69561a`  
		Last Modified: Mon, 01 Mar 2021 23:43:29 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

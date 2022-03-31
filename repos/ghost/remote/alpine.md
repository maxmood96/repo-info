## `ghost:alpine`

```console
$ docker pull ghost@sha256:4b17f9237d5e4349b84c0c0af4bb16c4a0ec9ed34223bb60fb6cf2fbb0dcf21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:be4d55bc891aac6ce702dc6d408b59c01c3e28db23db56b026ae4e5a82749ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118695095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69f1a46305fb4e85178ddd8a1c38329536cd7ba9082facdb9db9b50bf4311ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 17:02:46 GMT
ENV NODE_VERSION=14.19.1
# Tue, 29 Mar 2022 17:02:55 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 29 Mar 2022 17:02:55 GMT
ENV YARN_VERSION=1.22.17
# Tue, 29 Mar 2022 17:03:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 29 Mar 2022 17:03:00 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 29 Mar 2022 17:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:03:00 GMT
CMD ["node"]
# Wed, 30 Mar 2022 14:16:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 30 Mar 2022 14:16:54 GMT
RUN apk add --no-cache 		bash
# Wed, 30 Mar 2022 14:16:54 GMT
ENV NODE_ENV=production
# Wed, 30 Mar 2022 14:16:54 GMT
ENV GHOST_CLI_VERSION=1.19.2
# Wed, 30 Mar 2022 14:17:19 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 30 Mar 2022 14:17:20 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 30 Mar 2022 14:17:20 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 30 Mar 2022 14:17:20 GMT
ENV GHOST_VERSION=4.41.3
# Wed, 30 Mar 2022 14:18:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 30 Mar 2022 14:18:27 GMT
WORKDIR /var/lib/ghost
# Wed, 30 Mar 2022 14:18:27 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 30 Mar 2022 14:18:27 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 30 Mar 2022 14:18:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 14:18:27 GMT
EXPOSE 2368
# Wed, 30 Mar 2022 14:18:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ddb1c832026589b7a17f518bf927e3d5ad5a060a5f3a479e5ecf2daac0518d`  
		Last Modified: Tue, 29 Mar 2022 17:16:51 GMT  
		Size: 37.1 MB (37133069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41e48c0f581d87d40b94960ea3c00d44fa32d312cc27154c0fa7ac42f5c113d`  
		Last Modified: Tue, 29 Mar 2022 17:16:45 GMT  
		Size: 2.4 MB (2358385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3631e191ab780ea8cffbbf80f1acc4a4be9c2ab59c4b3a65413d48eddb6178c`  
		Last Modified: Tue, 29 Mar 2022 17:16:45 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2f92e7800d77c9bab43cdd0c5e7ee3fad81a5d0cefb9ab47b33084615ee6b`  
		Last Modified: Wed, 30 Mar 2022 14:19:10 GMT  
		Size: 11.2 KB (11207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171e4776fff9d84adb15a05b0eb445a71bd6e295f671c0b5f78d48367d43f64`  
		Last Modified: Wed, 30 Mar 2022 14:19:10 GMT  
		Size: 817.2 KB (817180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ec9b4c3890a3bc44cb00888f91deab34cb950079bc477dbc42d9de92437541`  
		Last Modified: Wed, 30 Mar 2022 14:19:13 GMT  
		Size: 9.6 MB (9569576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff729a4e9f6205fb574141ddeeea6d5de03d53009e45eace4368f3d039cd45b`  
		Last Modified: Wed, 30 Mar 2022 14:19:22 GMT  
		Size: 66.0 MB (65986325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794383f3ccfb8487207cd34a9ae62ac9773fee607a407b571bc7c18f6b1b80e9`  
		Last Modified: Wed, 30 Mar 2022 14:19:10 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:77fd71c33d7c47f43e7009e28cb25c9d00398a1401dd0060470f8805aa07bb50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119898800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cd0f86af02dd32a79fb7bdf347207566bd40a354afffb714564ca0e4ed8b0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:46:39 GMT
ENV NODE_VERSION=14.19.1
# Tue, 29 Mar 2022 11:02:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 29 Mar 2022 11:02:01 GMT
ENV YARN_VERSION=1.22.17
# Tue, 29 Mar 2022 11:02:09 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 29 Mar 2022 11:02:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 29 Mar 2022 11:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 11:02:10 GMT
CMD ["node"]
# Tue, 29 Mar 2022 19:50:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 19:50:49 GMT
RUN apk add --no-cache 		bash
# Tue, 29 Mar 2022 19:50:50 GMT
ENV NODE_ENV=production
# Tue, 29 Mar 2022 19:50:50 GMT
ENV GHOST_CLI_VERSION=1.19.2
# Tue, 29 Mar 2022 19:52:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 29 Mar 2022 19:52:06 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 29 Mar 2022 19:52:07 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 29 Mar 2022 19:52:07 GMT
ENV GHOST_VERSION=4.41.3
# Tue, 29 Mar 2022 20:01:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 29 Mar 2022 20:01:04 GMT
WORKDIR /var/lib/ghost
# Tue, 29 Mar 2022 20:01:04 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 29 Mar 2022 20:01:05 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 29 Mar 2022 20:01:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 20:01:06 GMT
EXPOSE 2368
# Tue, 29 Mar 2022 20:01:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877b49c75ab03c73d9140778f9727f84108b8a4cc32fafa2e88df4f95c527459`  
		Last Modified: Tue, 29 Mar 2022 11:58:25 GMT  
		Size: 36.2 MB (36198521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6c0be35453a526141b5f5ce8e8f101abc6f0ad933401163f308069bd5b6fee`  
		Last Modified: Tue, 29 Mar 2022 11:58:02 GMT  
		Size: 2.4 MB (2418475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdcf8f7d051ca95cbc88005eacc12358811aac56a67c4d7ccaae0f6d4c63932`  
		Last Modified: Tue, 29 Mar 2022 11:58:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052c794d1585fcdff9fb9a3955e7ad9180f46d736633cf9c775b6ac13bae7450`  
		Last Modified: Tue, 29 Mar 2022 20:01:48 GMT  
		Size: 11.0 KB (10971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d86ee12b07fef465211a1475e777e18aa3c025e5821fa5346a9a20684195c6`  
		Last Modified: Tue, 29 Mar 2022 20:01:48 GMT  
		Size: 771.2 KB (771178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858775256ecab84329e17328707637c6e02aa8c9c088afa51154054fe5eb99c6`  
		Last Modified: Tue, 29 Mar 2022 20:02:03 GMT  
		Size: 9.6 MB (9570483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864a0808e40067fc04a12532c619220efa0570486e05b606508e0809bd952fce`  
		Last Modified: Tue, 29 Mar 2022 20:03:00 GMT  
		Size: 68.3 MB (68302158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c091fd310a3f88169fad4541cae2bea2554ea3dc472dd7ec916c316ca30599`  
		Last Modified: Tue, 29 Mar 2022 20:01:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a15bd97d011bc8c5ccade0592aa61c35ab709c5d1551ceaef06083776e083337
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118657606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec469d6afeaccfe619b5613e9f659cc57ed8ad832f2d4a484bad77298d216b0`
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
# Fri, 25 Mar 2022 04:32:12 GMT
ENV GHOST_CLI_VERSION=1.19.2
# Fri, 25 Mar 2022 04:33:02 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Fri, 25 Mar 2022 04:33:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 25 Mar 2022 04:33:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 26 Mar 2022 01:05:52 GMT
ENV GHOST_VERSION=4.41.3
# Sat, 26 Mar 2022 01:13:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 26 Mar 2022 01:13:04 GMT
WORKDIR /var/lib/ghost
# Sat, 26 Mar 2022 01:13:05 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 26 Mar 2022 01:13:05 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 26 Mar 2022 01:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Mar 2022 01:13:06 GMT
EXPOSE 2368
# Sat, 26 Mar 2022 01:13:06 GMT
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
	-	`sha256:9d8bfabab2c907e94ee81e726e80b2d961c19251ba69f8b13271daa64227a1e3`  
		Last Modified: Fri, 25 Mar 2022 04:42:58 GMT  
		Size: 9.6 MB (9570120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7081a900652356421a87b4581ab16d2cf917d9c1d63fb6c951583eb57e6cca1`  
		Last Modified: Sat, 26 Mar 2022 01:16:38 GMT  
		Size: 67.8 MB (67772074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08444c3852580a30831c29efaefa38bb57c66d1276a3d0913c7a207c3525ccc5`  
		Last Modified: Sat, 26 Mar 2022 01:15:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:aa0940573b30b525a005147f913ded0c68aca978a2473a3f3bfadf094622ecd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138394558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ce60b34eab0056da0f7cd67e1d10cc371a35f0384794ec2a841e4b2e7e69a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 22:27:40 GMT
ENV NODE_VERSION=14.19.1
# Tue, 29 Mar 2022 22:54:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 29 Mar 2022 22:54:35 GMT
ENV YARN_VERSION=1.22.17
# Tue, 29 Mar 2022 22:54:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 29 Mar 2022 22:54:45 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 29 Mar 2022 22:54:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 22:54:46 GMT
CMD ["node"]
# Wed, 30 Mar 2022 21:46:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 30 Mar 2022 21:46:47 GMT
RUN apk add --no-cache 		bash
# Wed, 30 Mar 2022 21:46:48 GMT
ENV NODE_ENV=production
# Wed, 30 Mar 2022 21:46:49 GMT
ENV GHOST_CLI_VERSION=1.19.2
# Wed, 30 Mar 2022 21:47:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 30 Mar 2022 21:47:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 30 Mar 2022 21:47:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 30 Mar 2022 21:47:26 GMT
ENV GHOST_VERSION=4.41.3
# Wed, 30 Mar 2022 21:50:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 30 Mar 2022 21:50:54 GMT
WORKDIR /var/lib/ghost
# Wed, 30 Mar 2022 21:50:56 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 30 Mar 2022 21:50:59 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 30 Mar 2022 21:51:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 21:51:04 GMT
EXPOSE 2368
# Wed, 30 Mar 2022 21:51:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab2baf5b4ebdd5cd082f2f05f560b7998efa5e255155fff88585061e47305e`  
		Last Modified: Wed, 30 Mar 2022 00:31:31 GMT  
		Size: 37.0 MB (37013640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b63c492d0b4b42693d4cffdc0eb95174807e6d0137abdf8a062c6ac97cda0db`  
		Last Modified: Wed, 30 Mar 2022 00:31:25 GMT  
		Size: 2.4 MB (2425561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a195e905bc588745f1ae62f3443b59d6546681d4bacf46c641f732c2a8f69f`  
		Last Modified: Wed, 30 Mar 2022 00:31:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed405f6354ccea9927cd684eeac405b064e7e328490fb44aff30661cbe0adeaa`  
		Last Modified: Wed, 30 Mar 2022 21:52:04 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a40a7792f8e846ee3701138c46e1f01cd724d1924f74f12417c234c6927a8f`  
		Last Modified: Wed, 30 Mar 2022 21:52:04 GMT  
		Size: 826.3 KB (826305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9247a9c370716f0f6de312c7996f7bfa176be4eeb3c953faddc73f7b7b900105`  
		Last Modified: Wed, 30 Mar 2022 21:52:06 GMT  
		Size: 9.6 MB (9569353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32ce8ce34dbf844e265eea7687ad32da9189a1d5e967e7dc49d616c056160a8`  
		Last Modified: Wed, 30 Mar 2022 21:52:20 GMT  
		Size: 85.8 MB (85830210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e3e5634feea768baa2cb44c022a026c4d0a4cc404f41f27c05900ad7a23a9f`  
		Last Modified: Wed, 30 Mar 2022 21:52:04 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

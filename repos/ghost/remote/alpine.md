## `ghost:alpine`

```console
$ docker pull ghost@sha256:ed6e66d55af4bb81d4f3696c6ed7f0adf6f7a5aadf1172f6a54cf092950510ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4b9fc9f4de7a517f39c755eaa1edf4ce2a3767de386640695995d676b53a04e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118696147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0503176d9719517afee6cbe1f92816c30d212abdc74c3d655a580d0c324a25`
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
# Tue, 05 Apr 2022 15:54:31 GMT
ENV GHOST_CLI_VERSION=1.19.2
# Tue, 05 Apr 2022 15:54:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 05 Apr 2022 15:54:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 05 Apr 2022 15:54:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 05 Apr 2022 15:54:56 GMT
ENV GHOST_VERSION=4.41.3
# Tue, 05 Apr 2022 15:56:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 05 Apr 2022 15:56:03 GMT
WORKDIR /var/lib/ghost
# Tue, 05 Apr 2022 15:56:03 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 05 Apr 2022 15:56:03 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 05 Apr 2022 15:56:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 15:56:03 GMT
EXPOSE 2368
# Tue, 05 Apr 2022 15:56:03 GMT
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
	-	`sha256:5d920f12deab052c98f41da462a51ce7fb574259253b7a27ad24aa4d06530d22`  
		Last Modified: Tue, 05 Apr 2022 15:56:28 GMT  
		Size: 9.6 MB (9570087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d7cd5ecfc93db6e633af1dc61a5ffb57548d2aff0a35bf2f6cd8434cbf5041`  
		Last Modified: Tue, 05 Apr 2022 15:56:33 GMT  
		Size: 66.0 MB (65987165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03d3f57ff13ae4d4c0451ee7fc0a991c2f326dd589c3f212a90f51a69af3deb`  
		Last Modified: Tue, 05 Apr 2022 15:56:21 GMT  
		Size: 547.0 B  
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
$ docker pull ghost@sha256:71c98b4279b43d5a55f60b7dc1fb62c09dd08579926be952be1a6f515d118dc4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118653116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df17936e1cde92659d6b2d51609b363e011ed189946711996cf7ab5abe2e3f6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 29 Mar 2022 02:13:44 GMT
ADD file:4c399e6082c49459f8606095d7261eddd2bbaa65359199c3fdc4d2cc068a67f9 in / 
# Tue, 29 Mar 2022 02:13:44 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 18:10:18 GMT
ENV NODE_VERSION=14.19.1
# Wed, 30 Mar 2022 18:23:12 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="094790128069eccc9534214e7435c70bcafa221a0ef0f229c59418f8762704fa"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 30 Mar 2022 18:23:13 GMT
ENV YARN_VERSION=1.22.17
# Wed, 30 Mar 2022 18:23:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 30 Mar 2022 18:23:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 30 Mar 2022 18:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 18:23:22 GMT
CMD ["node"]
# Thu, 31 Mar 2022 18:20:22 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 31 Mar 2022 18:20:24 GMT
RUN apk add --no-cache 		bash
# Thu, 31 Mar 2022 18:20:25 GMT
ENV NODE_ENV=production
# Thu, 31 Mar 2022 18:20:25 GMT
ENV GHOST_CLI_VERSION=1.19.2
# Thu, 31 Mar 2022 18:21:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 31 Mar 2022 18:21:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 31 Mar 2022 18:21:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 31 Mar 2022 18:21:22 GMT
ENV GHOST_VERSION=4.41.3
# Thu, 31 Mar 2022 18:28:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip '::' --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python2 vips-dev; 				npm_config_python='python2' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 31 Mar 2022 18:28:34 GMT
WORKDIR /var/lib/ghost
# Thu, 31 Mar 2022 18:28:34 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 31 Mar 2022 18:28:35 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 31 Mar 2022 18:28:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 18:28:35 GMT
EXPOSE 2368
# Thu, 31 Mar 2022 18:28:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:994307ea7bfd1233222fa14c4fc32b8b85be60f9840c03fba9299eb918066ef3`  
		Last Modified: Tue, 29 Mar 2022 02:15:47 GMT  
		Size: 2.4 MB (2427966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4a0bb724668bbb22817bd44c2ce897e0300fb938a1af28ae0de841a5d04fc8`  
		Last Modified: Wed, 30 Mar 2022 19:44:38 GMT  
		Size: 35.8 MB (35750762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c798af73b3d1c7d446093386a0689154ddd4481f8586c69931d4d134920b6`  
		Last Modified: Wed, 30 Mar 2022 19:44:14 GMT  
		Size: 2.4 MB (2418235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977d90ccd1d916b11c878f2b539f9a2e7aca8ef60f2309f47b6e11b03be15262`  
		Last Modified: Wed, 30 Mar 2022 19:44:13 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b027f88dcffaefc45bc0ea64cfa2d94a59900f2cc4af34f64235d3bf42fe904`  
		Last Modified: Thu, 31 Mar 2022 18:30:54 GMT  
		Size: 10.8 KB (10768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0fd977c66b0d120854c387342086c6cd3062b2b42ba5df3d1ec5926c30e0d0`  
		Last Modified: Thu, 31 Mar 2022 18:30:54 GMT  
		Size: 704.1 KB (704130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba33f110062a4e4e27f084ddc720aae76b512967c1507821bcd00b7264ae7`  
		Last Modified: Thu, 31 Mar 2022 18:31:09 GMT  
		Size: 9.6 MB (9570071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa2aac1f4b608b2d451f1321ebb859cf9d908b13a8df2e6f27c100f0bfe7f72`  
		Last Modified: Thu, 31 Mar 2022 18:32:05 GMT  
		Size: 67.8 MB (67770188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990d422723179bb312a1726321499a2d0b3ac26caa062bff5a2f8df225e90fad`  
		Last Modified: Thu, 31 Mar 2022 18:30:54 GMT  
		Size: 546.0 B  
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

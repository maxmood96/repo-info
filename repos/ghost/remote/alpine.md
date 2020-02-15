## `ghost:alpine`

```console
$ docker pull ghost@sha256:9edd61e58a1cb2b1f965079a4b3128b6631dfffd2af28673120a3ed44dc87ac0
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

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5f6bc81961f3ebccb3207b79484e59e4b72f2d325e0a61bc119d4ae91362800b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97139145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a75d3cd55e4216e80099934062ea4bd1b525b3dfb065f168f2854e8e404ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2020 23:29:17 GMT
ENV NODE_VERSION=12.16.0
# Wed, 12 Feb 2020 23:29:28 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 12 Feb 2020 23:29:28 GMT
ENV YARN_VERSION=1.22.0
# Wed, 12 Feb 2020 23:29:32 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 12 Feb 2020 23:29:33 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 12 Feb 2020 23:29:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2020 23:29:34 GMT
CMD ["node"]
# Wed, 12 Feb 2020 23:54:01 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 12 Feb 2020 23:54:05 GMT
RUN apk add --no-cache 		bash
# Wed, 12 Feb 2020 23:54:05 GMT
ENV NODE_ENV=production
# Wed, 12 Feb 2020 23:54:06 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Wed, 12 Feb 2020 23:54:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 12 Feb 2020 23:54:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 12 Feb 2020 23:54:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 15 Feb 2020 01:20:44 GMT
ENV GHOST_VERSION=3.6.0
# Sat, 15 Feb 2020 01:21:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 15 Feb 2020 01:21:41 GMT
WORKDIR /var/lib/ghost
# Sat, 15 Feb 2020 01:21:41 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 15 Feb 2020 01:21:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 15 Feb 2020 01:21:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Feb 2020 01:21:41 GMT
EXPOSE 2368
# Sat, 15 Feb 2020 01:21:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c818a1969a4b15d54d3cffdcde976cb76523719dc0cb764a749a85a4917c6f`  
		Last Modified: Wed, 12 Feb 2020 23:35:02 GMT  
		Size: 24.5 MB (24490053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fced71a1b5bcff57e826487fffa79f8b4c451376734c4dfa0cf83ad131edf4f1`  
		Last Modified: Wed, 12 Feb 2020 23:34:54 GMT  
		Size: 1.3 MB (1265387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799240489e66f7669e8b51729ee6f31b8c95e08cd9f0024c65629056d903207b`  
		Last Modified: Wed, 12 Feb 2020 23:34:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b46485691f988d376a6f0ad7e85fd1df0efbde172cc8da3a58e352b5fbbe90`  
		Last Modified: Wed, 12 Feb 2020 23:57:25 GMT  
		Size: 9.9 KB (9905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b35a081885fc995b489c82d8624d7ed380058b626ab98c7756a9aa80f10ea8`  
		Last Modified: Wed, 12 Feb 2020 23:57:26 GMT  
		Size: 1.2 MB (1211025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b3499c94082cfab565f69b21a18de8c5e25213ee2b7af4bbae53961f206e3`  
		Last Modified: Wed, 12 Feb 2020 23:57:31 GMT  
		Size: 6.8 MB (6789967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754d9b2f3d226aebc1e5a43d038517a546dfcf2fc6c5535fe7d1e02daa9646a6`  
		Last Modified: Sat, 15 Feb 2020 01:22:42 GMT  
		Size: 60.6 MB (60569019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2144d83363bcccaabc70f2f38a7b0b430a9e8ff9a8b4c610f5caccad4c69`  
		Last Modified: Sat, 15 Feb 2020 01:22:29 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:4dabd944583ff14f599037c91350244b35b950ae0189e5a1cb99cb5a0f3537a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88565195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eae0c6514eaa7a997a3051df2bde860c0ac1bdfee88b776caa1aff0739c5e06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2020 23:22:29 GMT
ENV NODE_VERSION=12.16.0
# Wed, 12 Feb 2020 23:33:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 12 Feb 2020 23:33:05 GMT
ENV YARN_VERSION=1.22.0
# Wed, 12 Feb 2020 23:33:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 12 Feb 2020 23:33:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 12 Feb 2020 23:33:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2020 23:33:12 GMT
CMD ["node"]
# Thu, 13 Feb 2020 00:04:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 13 Feb 2020 00:04:30 GMT
RUN apk add --no-cache 		bash
# Thu, 13 Feb 2020 00:04:32 GMT
ENV NODE_ENV=production
# Thu, 13 Feb 2020 00:04:34 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Thu, 13 Feb 2020 00:05:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 13 Feb 2020 00:05:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 13 Feb 2020 00:05:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 13 Feb 2020 00:05:24 GMT
ENV GHOST_VERSION=3.5.2
# Thu, 13 Feb 2020 00:11:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 13 Feb 2020 00:11:49 GMT
WORKDIR /var/lib/ghost
# Thu, 13 Feb 2020 00:11:51 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 13 Feb 2020 00:11:51 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 13 Feb 2020 00:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2020 00:11:54 GMT
EXPOSE 2368
# Thu, 13 Feb 2020 00:11:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5678fd9f2c6488b8ec00512ecd089ab985c5c1ea4cbd35ed421d6a5dffcdaba`  
		Last Modified: Wed, 12 Feb 2020 23:34:45 GMT  
		Size: 23.9 MB (23934055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7ca6afecf94810b0ae0ccd5755fd2e5a8b53f9f85a031e0231e4a3ab892616`  
		Last Modified: Wed, 12 Feb 2020 23:34:36 GMT  
		Size: 1.3 MB (1328555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeea266db1607039a4f5d809fd8e69bdd0cecd1a370becdfcef44f0added8a47`  
		Last Modified: Wed, 12 Feb 2020 23:34:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11367f9a4964bba6d463d453fdf58f3c9773f2d015c38c490968d00411ac29a3`  
		Last Modified: Thu, 13 Feb 2020 00:12:34 GMT  
		Size: 9.7 KB (9734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ffea782a84194fbba007306cfad31222fb788915f8994870b7c2cc0fb5161b`  
		Last Modified: Thu, 13 Feb 2020 00:12:33 GMT  
		Size: 1.2 MB (1162976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da7be24138ffdad1eb28954cbda3bdbd79faddbee7732b1a5783f010a0d7fe4`  
		Last Modified: Thu, 13 Feb 2020 00:12:37 GMT  
		Size: 6.8 MB (6790784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee27b2a79fa0718e9074a16f6df7ff602411f332d519b496296a136e84209a6`  
		Last Modified: Thu, 13 Feb 2020 00:12:59 GMT  
		Size: 52.7 MB (52720704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241df7bf0dfa228414b5c6e3952c84a1785cbcfacaa0cdac65fd91f1dd0db212`  
		Last Modified: Thu, 13 Feb 2020 00:12:33 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:47a1530197e3649433c7e9abdc28128464ca070a507cbc831e98e4e0954ae265
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86955757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96bc31f1a7aa51995dbe494e696796472a85d11c679a767af11ff8514dedc90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2020 23:35:59 GMT
ENV NODE_VERSION=12.16.0
# Wed, 12 Feb 2020 23:44:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 12 Feb 2020 23:44:45 GMT
ENV YARN_VERSION=1.22.0
# Wed, 12 Feb 2020 23:44:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 12 Feb 2020 23:44:51 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 12 Feb 2020 23:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2020 23:44:52 GMT
CMD ["node"]
# Thu, 13 Feb 2020 00:11:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 13 Feb 2020 00:11:04 GMT
RUN apk add --no-cache 		bash
# Thu, 13 Feb 2020 00:11:05 GMT
ENV NODE_ENV=production
# Thu, 13 Feb 2020 00:11:05 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Thu, 13 Feb 2020 00:11:32 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 13 Feb 2020 00:11:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 13 Feb 2020 00:11:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 15 Feb 2020 00:57:53 GMT
ENV GHOST_VERSION=3.6.0
# Sat, 15 Feb 2020 01:02:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 15 Feb 2020 01:02:21 GMT
WORKDIR /var/lib/ghost
# Sat, 15 Feb 2020 01:02:21 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 15 Feb 2020 01:02:22 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 15 Feb 2020 01:02:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Feb 2020 01:02:23 GMT
EXPOSE 2368
# Sat, 15 Feb 2020 01:02:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b4dc654f394e621316254b86841a6e9ce6a437bd4a56a55299a460cdfc5d2`  
		Last Modified: Wed, 12 Feb 2020 23:49:17 GMT  
		Size: 23.5 MB (23497484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492668007554ff181b33f19c1bdcc5415235d5bc92c26c4c5da9804581ce9029`  
		Last Modified: Wed, 12 Feb 2020 23:49:09 GMT  
		Size: 1.3 MB (1328487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c603a1cfd0b0165fd4af71d7832fc333032e97dc7c8aad8ab77bcf70e5e91f9c`  
		Last Modified: Wed, 12 Feb 2020 23:49:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259bdbed2e189fb35e8f9ef65d6832cb93b1689ae3b7bba0eebaf6decb19bbe6`  
		Last Modified: Thu, 13 Feb 2020 00:16:45 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a807d01accc045e442ed52a9c4cb6086528a7f7e0d2338c844f4dfa16016bb2b`  
		Last Modified: Thu, 13 Feb 2020 00:16:46 GMT  
		Size: 1.1 MB (1101438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43203eb69316278c03f902f3fed944237469736af4562ffdf766587cfa90d12f`  
		Last Modified: Thu, 13 Feb 2020 00:16:50 GMT  
		Size: 6.8 MB (6790097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca5f3f376a561aabd27a749d6544adbe18a3efb59b0f44817573c87316ed168`  
		Last Modified: Sat, 15 Feb 2020 01:03:34 GMT  
		Size: 51.8 MB (51808346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c910ff4dcd90598521e0cc16409aa8f2dca1b46ca4dab69587f02c05a2995`  
		Last Modified: Sat, 15 Feb 2020 01:03:07 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:911cab464b0ca0fcdd011859482503401ac54e43ef0f873a94719c90407a11d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89745810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb89cb9dffdf20c76d1e4a3a6ebd1552f6655ab5e26b891fc73aac567c7bd34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2020 23:08:25 GMT
ENV NODE_VERSION=12.16.0
# Wed, 12 Feb 2020 23:19:34 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 12 Feb 2020 23:19:37 GMT
ENV YARN_VERSION=1.22.0
# Wed, 12 Feb 2020 23:19:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 12 Feb 2020 23:19:45 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 12 Feb 2020 23:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2020 23:19:48 GMT
CMD ["node"]
# Wed, 12 Feb 2020 23:50:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 12 Feb 2020 23:50:06 GMT
RUN apk add --no-cache 		bash
# Wed, 12 Feb 2020 23:50:07 GMT
ENV NODE_ENV=production
# Wed, 12 Feb 2020 23:50:07 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Wed, 12 Feb 2020 23:50:30 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 12 Feb 2020 23:50:32 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 12 Feb 2020 23:50:32 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 12 Feb 2020 23:50:33 GMT
ENV GHOST_VERSION=3.5.2
# Wed, 12 Feb 2020 23:54:51 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 12 Feb 2020 23:54:57 GMT
WORKDIR /var/lib/ghost
# Wed, 12 Feb 2020 23:54:58 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 12 Feb 2020 23:54:59 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 12 Feb 2020 23:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2020 23:55:02 GMT
EXPOSE 2368
# Wed, 12 Feb 2020 23:55:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7097de652fb572d997945fb1d27f38261a912e1015acdf09ff6d114eed5c998`  
		Last Modified: Wed, 12 Feb 2020 23:26:07 GMT  
		Size: 24.7 MB (24664135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559dfd9420015f9f41cb99c660d8a2c224f0bdce88a8be5d082492f550d06121`  
		Last Modified: Wed, 12 Feb 2020 23:25:56 GMT  
		Size: 1.3 MB (1328535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5caeac1500e8972bc7c4dadb6ba2ab41b08d4b5ce4527bb357002d06de9645d6`  
		Last Modified: Wed, 12 Feb 2020 23:25:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0145713359853ad33525266275ab122149e7270afd2435228245ac100ebcd5bb`  
		Last Modified: Wed, 12 Feb 2020 23:56:29 GMT  
		Size: 9.9 KB (9853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84426e6bd04a09e88006ef5e4354ed896ecee57e69f923b0bbf0d52e7cdf900d`  
		Last Modified: Wed, 12 Feb 2020 23:56:29 GMT  
		Size: 1.2 MB (1223202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae0f5d90880bb7fafb6b5bedcd508cc9c58a69a75ed4165d9a556e828451496`  
		Last Modified: Wed, 12 Feb 2020 23:56:33 GMT  
		Size: 6.8 MB (6789855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff71cf73ce1b38a613e2bbed48aa89e94a09b7d744e35fd482e24daec75c7062`  
		Last Modified: Wed, 12 Feb 2020 23:56:51 GMT  
		Size: 53.0 MB (53006329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1147fafa848e38d3e5569b4b6b9a6c8fabb4f0c962b1fab2572140cbe8d2b210`  
		Last Modified: Wed, 12 Feb 2020 23:56:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; 386

```console
$ docker pull ghost@sha256:ef6d16c732cf93316d3f8acd6b739f36486629d25e7bf86e88682b033820623b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90201643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f8d1adb1b15a2c20abf5cf24338ce81aeeeb883576266d06717d60663c539c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2020 00:00:15 GMT
ENV NODE_VERSION=12.16.0
# Thu, 13 Feb 2020 00:40:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Thu, 13 Feb 2020 00:40:01 GMT
ENV YARN_VERSION=1.22.0
# Thu, 13 Feb 2020 00:40:03 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Thu, 13 Feb 2020 00:40:03 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 13 Feb 2020 00:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2020 00:40:04 GMT
CMD ["node"]
# Thu, 13 Feb 2020 00:56:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 13 Feb 2020 00:56:51 GMT
RUN apk add --no-cache 		bash
# Thu, 13 Feb 2020 00:56:51 GMT
ENV NODE_ENV=production
# Thu, 13 Feb 2020 00:56:51 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Thu, 13 Feb 2020 00:57:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 13 Feb 2020 00:57:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 13 Feb 2020 00:57:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 15 Feb 2020 01:38:28 GMT
ENV GHOST_VERSION=3.6.0
# Sat, 15 Feb 2020 01:41:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 15 Feb 2020 01:41:27 GMT
WORKDIR /var/lib/ghost
# Sat, 15 Feb 2020 01:41:28 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 15 Feb 2020 01:41:28 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 15 Feb 2020 01:41:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Feb 2020 01:41:28 GMT
EXPOSE 2368
# Sat, 15 Feb 2020 01:41:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32ffb92410081fba3961c52b2a7a5d0208b929e5fd9cf8d0dba4ad38b35d76`  
		Last Modified: Thu, 13 Feb 2020 00:41:10 GMT  
		Size: 24.8 MB (24804929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da37c2099bc04c316683f26afac94c1c53b9d9c8c1da04508dc3ec4d2c3b5a9e`  
		Last Modified: Thu, 13 Feb 2020 00:41:04 GMT  
		Size: 1.3 MB (1328530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c3adfb3f10e3193ab6d3f21dad9ed2e1aafc84112e99cdeb80b34763172fa6`  
		Last Modified: Thu, 13 Feb 2020 00:41:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67779fdb1c4dc4f17ca44f9fb8e0b2e5ca317234c17063f9664fd17c6c52d1dd`  
		Last Modified: Thu, 13 Feb 2020 01:00:31 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6722520a7670ee3e3c4f5df9fa3e476afab8807d0a0eb4f24caf6719aac46132`  
		Last Modified: Thu, 13 Feb 2020 01:00:32 GMT  
		Size: 1.3 MB (1261247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882fff1fe75451a660a8ae3b7fc0f61ffa13767af37557a2b03e3cba2977fbda`  
		Last Modified: Thu, 13 Feb 2020 01:00:35 GMT  
		Size: 6.8 MB (6789916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ce327ca376828c5b4f93475b84d86b44d5443abd7be0acef5fd4069839225f`  
		Last Modified: Sat, 15 Feb 2020 01:42:15 GMT  
		Size: 53.2 MB (53199661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b07e1d2809b82e84a75f6c1be95a4799a3db60ad201bdf94f1fa872a7485f4`  
		Last Modified: Sat, 15 Feb 2020 01:41:57 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; ppc64le

```console
$ docker pull ghost@sha256:36dc60b96ec7d9ea02d54cc37fd961da72bb5f4980fc2c65a5683a50943ab0dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93861804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5246b22b522d753821c2f5b077e0e8c51622e182d89e1f49728fb37fb493fa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2020 00:05:18 GMT
ENV NODE_VERSION=12.16.0
# Thu, 13 Feb 2020 00:22:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Thu, 13 Feb 2020 00:22:19 GMT
ENV YARN_VERSION=1.22.0
# Thu, 13 Feb 2020 00:22:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Thu, 13 Feb 2020 00:22:29 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 13 Feb 2020 00:22:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2020 00:22:32 GMT
CMD ["node"]
# Thu, 13 Feb 2020 00:52:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 13 Feb 2020 00:53:00 GMT
RUN apk add --no-cache 		bash
# Thu, 13 Feb 2020 00:53:02 GMT
ENV NODE_ENV=production
# Thu, 13 Feb 2020 00:53:05 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Thu, 13 Feb 2020 00:53:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 13 Feb 2020 00:53:42 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 13 Feb 2020 00:53:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 15 Feb 2020 01:22:50 GMT
ENV GHOST_VERSION=3.6.0
# Sat, 15 Feb 2020 01:26:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 15 Feb 2020 01:26:59 GMT
WORKDIR /var/lib/ghost
# Sat, 15 Feb 2020 01:27:04 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 15 Feb 2020 01:27:05 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 15 Feb 2020 01:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Feb 2020 01:27:12 GMT
EXPOSE 2368
# Sat, 15 Feb 2020 01:27:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c8eea8fec2b26a8cb1d5c10e07cc9127b3ef92a16aac394285ab2adb076920`  
		Last Modified: Thu, 13 Feb 2020 00:28:46 GMT  
		Size: 26.8 MB (26799288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825188287683677000de4197612ea7b0d87b67c35607bea7e016ac7350027377`  
		Last Modified: Thu, 13 Feb 2020 00:28:40 GMT  
		Size: 1.3 MB (1328520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aea89b03d2ef60624b449fe42446e8eea5e38370a8df4b4f84381edd3885b`  
		Last Modified: Thu, 13 Feb 2020 00:28:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a2ef6270661ca7c868680a59594a05b7b0e4d1a66020b2528124c718deea97`  
		Last Modified: Thu, 13 Feb 2020 00:59:47 GMT  
		Size: 10.4 KB (10395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e71cc79f6707acdab155471b2f7edb85de263cacc9e182ad55bd1ac2c5fe456`  
		Last Modified: Thu, 13 Feb 2020 00:59:49 GMT  
		Size: 1.3 MB (1293098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bb9086b3c904e01e0c821fa313da3a13f6c486ad1fced506d7f1efb113b1c5`  
		Last Modified: Thu, 13 Feb 2020 00:59:51 GMT  
		Size: 6.8 MB (6789904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b518646eaf6be53175c8c5844ad635746e3148083486d17c3ce7b46e601a699`  
		Last Modified: Sat, 15 Feb 2020 01:29:51 GMT  
		Size: 54.8 MB (54817648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf507328272cb61aea711f1ca760521bb8e6e4b98ad0e10927f5017596e493c`  
		Last Modified: Sat, 15 Feb 2020 01:29:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; s390x

```console
$ docker pull ghost@sha256:fbc96b3da00a878b9e70f8446d8cf0aaa8bcea7202ad1183e34a7f374b242421
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89338244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7682fbe464ce28a65f55a4fe23400fcf1467f119549d218f9f0d25dd21640d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2020 23:33:41 GMT
ENV NODE_VERSION=12.16.0
# Wed, 12 Feb 2020 23:54:21 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c7c38c170c38a491ecffbd5324415818f88abc2a6a79076493c1028a19bf64df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 12 Feb 2020 23:54:24 GMT
ENV YARN_VERSION=1.22.0
# Wed, 12 Feb 2020 23:54:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 12 Feb 2020 23:54:27 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 12 Feb 2020 23:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2020 23:54:28 GMT
CMD ["node"]
# Thu, 13 Feb 2020 00:34:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 13 Feb 2020 00:34:58 GMT
RUN apk add --no-cache 		bash
# Thu, 13 Feb 2020 00:34:59 GMT
ENV NODE_ENV=production
# Thu, 13 Feb 2020 00:35:00 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Thu, 13 Feb 2020 00:35:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 13 Feb 2020 00:35:30 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 13 Feb 2020 00:35:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 13 Feb 2020 00:35:31 GMT
ENV GHOST_VERSION=3.5.2
# Thu, 13 Feb 2020 00:38:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 13 Feb 2020 00:38:38 GMT
WORKDIR /var/lib/ghost
# Thu, 13 Feb 2020 00:38:39 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 13 Feb 2020 00:38:39 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 13 Feb 2020 00:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2020 00:38:41 GMT
EXPOSE 2368
# Thu, 13 Feb 2020 00:38:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c82f94cfd4d59ee862ff77cb92f5da5284f8e77bdeca93a6f80bd2192de1a`  
		Last Modified: Wed, 12 Feb 2020 23:57:59 GMT  
		Size: 24.6 MB (24569175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbf4cfe54b65f7368a2d928c26c9e9a022247eb970520986e663d1f5174627`  
		Last Modified: Wed, 12 Feb 2020 23:57:54 GMT  
		Size: 1.3 MB (1328501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed08fd7f5dbd02434176974dbd62e1416a55a1dbc5a55c14078e2d694f8707d`  
		Last Modified: Wed, 12 Feb 2020 23:57:54 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60ed276d62dfa40eac5103eb9c32daa54582b9e6149e8c1e6a55905d1e6e7c5`  
		Last Modified: Thu, 13 Feb 2020 00:39:51 GMT  
		Size: 10.0 KB (9989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e4b78b8fe523c2b8089d0c8f9e0f6281bd82a2e75eefaeced1b9959bf8cb29`  
		Last Modified: Thu, 13 Feb 2020 00:39:56 GMT  
		Size: 1.2 MB (1245284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0442952ff0c293101940e447d362dae1faf34e247571ed287e050ce99824b5dc`  
		Last Modified: Thu, 13 Feb 2020 00:39:52 GMT  
		Size: 6.8 MB (6789953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7465937ce988e5a0e5818e3d73d99994b7cb46ea81a4d27457a401a445e554c`  
		Last Modified: Thu, 13 Feb 2020 00:40:06 GMT  
		Size: 52.8 MB (52812488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d17f425e19acbaf45ff92f011bf406a3a72e0e08b902dab5fe2ed94316c855`  
		Last Modified: Thu, 13 Feb 2020 00:40:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

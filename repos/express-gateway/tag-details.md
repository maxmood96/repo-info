<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `express-gateway`

-	[`express-gateway:1.16.11`](#express-gateway11611)
-	[`express-gateway:1.16.x`](#express-gateway116x)
-	[`express-gateway:1.x`](#express-gateway1x)
-	[`express-gateway:latest`](#express-gatewaylatest)

## `express-gateway:1.16.11`

```console
$ docker pull express-gateway@sha256:367d4ac9dbd77a44b280e66d80be62697431a5ed87686c916283b8797845945a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.16.11` - linux; amd64

```console
$ docker pull express-gateway@sha256:b1bad91f6d5a13e41a48d1ec8ecdd6b7e19beec82442f90a008f67a7a8b3921c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39556032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dc911ce70e6d71e8f133d9bbdaf7dcc75893568429420b58a5849150ee0f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:59:28 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 17:59:28 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 17:59:45 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 17:59:46 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 17:59:46 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 17:59:47 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 17:59:47 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 17:59:47 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:59:47 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fb847bc81fd2087a0ad97758300d091b6e92a43bcfc5546dbfd23f913e43b0`  
		Last Modified: Wed, 07 Jul 2021 18:00:05 GMT  
		Size: 9.9 MB (9898550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ecdcfd1afec27a31d62ada59ea53ec9f7cf82856a06e7af755b456a1b990a0`  
		Last Modified: Wed, 07 Jul 2021 18:00:02 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.11` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:76403d126c69fa2b67caafeeead58bc990e8b7ef6478820cba7750903729d489
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39654510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33bfd0aa6700ed5c58d3f45b35dd037639eff716ed1643d6f9acbb9cd4f51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:21:10 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 04:49:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 04:49:02 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 04:49:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 04:49:07 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 04:49:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 04:49:08 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:36:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:36:11 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:36:29 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:36:30 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:36:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:36:31 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:36:31 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:36:31 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:36:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:36:31 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea3779ab6047f8155b959727d18ea94cc5468e381fa4b6e589b41847bee610c`  
		Last Modified: Wed, 07 Jul 2021 05:33:10 GMT  
		Size: 24.7 MB (24729422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53cc19e504a9644d8a550e441c5f7c441eab66310bbfacb9bee0dc18a53572e`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 2.3 MB (2299356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2e06d2bdcce894629edb871383d5e50387496101290cbf487255746af66d4d`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926150d403084ea7fcd6c97c4e109769961ac9865e347b3be2471a49cca504a`  
		Last Modified: Wed, 07 Jul 2021 05:36:54 GMT  
		Size: 9.9 MB (9898027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c92afc4de53f859121fdc0cf49038122469b118b51a85fb82777c5820c2fe6e`  
		Last Modified: Wed, 07 Jul 2021 05:36:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.11` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:e876ffb4fc41c7ae5b37eb7b841356d0e5ac9e2ec68843cbe2914e6bc7b8a027
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41905682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dfcb2361e91576bef7b8021e64741af100c9f407600f4b87320b948e9e1113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:38 GMT
ADD file:91004afe9c028e9c999ada226de52c8f6a429c745e4dfe0502eab6e63fee09b1 in / 
# Wed, 14 Apr 2021 19:31:44 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 03:18:28 GMT
ENV NODE_VERSION=12.22.1
# Sun, 27 Jun 2021 03:37:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b7c8a2cb26790b4cc21a69ea5896ecb3e88712a35dcd5f3ef1c799214ad1f5da"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sun, 27 Jun 2021 03:37:14 GMT
ENV YARN_VERSION=1.22.5
# Sun, 27 Jun 2021 03:37:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sun, 27 Jun 2021 03:37:30 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 27 Jun 2021 03:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 03:37:51 GMT
CMD ["node"]
# Sun, 27 Jun 2021 19:39:53 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Sun, 27 Jun 2021 19:39:59 GMT
ARG EG_VERSION=1.16.11
# Sun, 27 Jun 2021 19:41:05 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Sun, 27 Jun 2021 19:41:15 GMT
ENV NODE_ENV=production
# Sun, 27 Jun 2021 19:41:22 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Sun, 27 Jun 2021 19:41:26 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Sun, 27 Jun 2021 19:41:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Sun, 27 Jun 2021 19:41:36 GMT
VOLUME [/var/lib/eg]
# Sun, 27 Jun 2021 19:41:40 GMT
EXPOSE 8080 9876
# Sun, 27 Jun 2021 19:41:44 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Sun, 27 Jun 2021 19:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 19:41:55 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:3be5611c0e64110909576b6b123a979626cbd064adb316722e45cebf5429ba51`  
		Last Modified: Wed, 14 Apr 2021 19:33:01 GMT  
		Size: 2.8 MB (2823734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bbd7a57bf45662270e7a86ebda57e981d07009529d9415c5ab6edb6916e6e1`  
		Last Modified: Sun, 27 Jun 2021 04:17:16 GMT  
		Size: 26.9 MB (26885597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f06e577e6e46168a31d1062509799d0d4378836bfc7ed69cc7d58ec0e3984d`  
		Last Modified: Sun, 27 Jun 2021 04:17:11 GMT  
		Size: 2.3 MB (2296917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd49437458087223d0c7e45c42bb1fac7f674b614135b908bc81ab7e5bfa37b`  
		Last Modified: Sun, 27 Jun 2021 04:17:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a63fb2c906dff6e0372a6fb36a267af33a6f6f838e7053e8d0d0649f1b297bd`  
		Last Modified: Sun, 27 Jun 2021 19:42:21 GMT  
		Size: 9.9 MB (9898657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1505c4888e140d303da5c76397170ed4c70cd24f9426f17a355db51c856ee8c5`  
		Last Modified: Sun, 27 Jun 2021 19:42:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.11` - linux; s390x

```console
$ docker pull express-gateway@sha256:11add88677afc864d02ffbac3b1529ded61d5dab95bc4179419a73a614170d7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39424451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223f1c874f82ab8a0aced01f13ce74dd0c0e0f92d1cdc9b80dfc4cc06940d05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:48 GMT
ADD file:f01bbceaff31cff54d8147154b6fc2938fd2d9866e90147689bd0b2c39e3ba5f in / 
# Wed, 14 Apr 2021 18:41:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:38:55 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 05:01:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 05:02:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 05:02:09 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 05:02:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:02:11 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:50:16 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:50:16 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:50:39 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:50:41 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:50:42 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:50:42 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:50:42 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:50:42 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:50:43 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:50:43 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:50:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:50:44 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:01bec321d6f53c2537689093496de5b1b149c5f1b25b80c786c537b3e153dbb8`  
		Last Modified: Wed, 14 Apr 2021 18:42:32 GMT  
		Size: 2.6 MB (2584667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d693e481a9cbde501cc1e06670a6f86b34f6f79853bf8fdc541b834dc6d4a83`  
		Last Modified: Wed, 07 Jul 2021 05:35:01 GMT  
		Size: 24.6 MB (24638654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73c01ec51af6cb4229ac118c0b7b0d67ce31fdb2677a3014cea73cb1728ad`  
		Last Modified: Wed, 07 Jul 2021 05:34:58 GMT  
		Size: 2.3 MB (2301691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed5f847e806f775a1b283645005c9770655edd8b79b7b218b84c2c72f2df0b5`  
		Last Modified: Wed, 07 Jul 2021 05:34:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3341322fc9e42c6b702520ede0f63ff227f7a3f41a1cebc93cb95c936e67bc27`  
		Last Modified: Wed, 07 Jul 2021 05:51:07 GMT  
		Size: 9.9 MB (9898658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462f2601717e3efc30e1c4e6261686ee5513c1d4f36a10f3aa2faa89849213e5`  
		Last Modified: Wed, 07 Jul 2021 05:51:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:1.16.x`

```console
$ docker pull express-gateway@sha256:367d4ac9dbd77a44b280e66d80be62697431a5ed87686c916283b8797845945a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.16.x` - linux; amd64

```console
$ docker pull express-gateway@sha256:b1bad91f6d5a13e41a48d1ec8ecdd6b7e19beec82442f90a008f67a7a8b3921c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39556032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dc911ce70e6d71e8f133d9bbdaf7dcc75893568429420b58a5849150ee0f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:59:28 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 17:59:28 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 17:59:45 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 17:59:46 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 17:59:46 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 17:59:47 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 17:59:47 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 17:59:47 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:59:47 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fb847bc81fd2087a0ad97758300d091b6e92a43bcfc5546dbfd23f913e43b0`  
		Last Modified: Wed, 07 Jul 2021 18:00:05 GMT  
		Size: 9.9 MB (9898550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ecdcfd1afec27a31d62ada59ea53ec9f7cf82856a06e7af755b456a1b990a0`  
		Last Modified: Wed, 07 Jul 2021 18:00:02 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:76403d126c69fa2b67caafeeead58bc990e8b7ef6478820cba7750903729d489
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39654510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33bfd0aa6700ed5c58d3f45b35dd037639eff716ed1643d6f9acbb9cd4f51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:21:10 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 04:49:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 04:49:02 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 04:49:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 04:49:07 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 04:49:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 04:49:08 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:36:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:36:11 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:36:29 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:36:30 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:36:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:36:31 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:36:31 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:36:31 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:36:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:36:31 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea3779ab6047f8155b959727d18ea94cc5468e381fa4b6e589b41847bee610c`  
		Last Modified: Wed, 07 Jul 2021 05:33:10 GMT  
		Size: 24.7 MB (24729422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53cc19e504a9644d8a550e441c5f7c441eab66310bbfacb9bee0dc18a53572e`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 2.3 MB (2299356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2e06d2bdcce894629edb871383d5e50387496101290cbf487255746af66d4d`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926150d403084ea7fcd6c97c4e109769961ac9865e347b3be2471a49cca504a`  
		Last Modified: Wed, 07 Jul 2021 05:36:54 GMT  
		Size: 9.9 MB (9898027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c92afc4de53f859121fdc0cf49038122469b118b51a85fb82777c5820c2fe6e`  
		Last Modified: Wed, 07 Jul 2021 05:36:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:e876ffb4fc41c7ae5b37eb7b841356d0e5ac9e2ec68843cbe2914e6bc7b8a027
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41905682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dfcb2361e91576bef7b8021e64741af100c9f407600f4b87320b948e9e1113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:38 GMT
ADD file:91004afe9c028e9c999ada226de52c8f6a429c745e4dfe0502eab6e63fee09b1 in / 
# Wed, 14 Apr 2021 19:31:44 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 03:18:28 GMT
ENV NODE_VERSION=12.22.1
# Sun, 27 Jun 2021 03:37:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b7c8a2cb26790b4cc21a69ea5896ecb3e88712a35dcd5f3ef1c799214ad1f5da"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sun, 27 Jun 2021 03:37:14 GMT
ENV YARN_VERSION=1.22.5
# Sun, 27 Jun 2021 03:37:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sun, 27 Jun 2021 03:37:30 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 27 Jun 2021 03:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 03:37:51 GMT
CMD ["node"]
# Sun, 27 Jun 2021 19:39:53 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Sun, 27 Jun 2021 19:39:59 GMT
ARG EG_VERSION=1.16.11
# Sun, 27 Jun 2021 19:41:05 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Sun, 27 Jun 2021 19:41:15 GMT
ENV NODE_ENV=production
# Sun, 27 Jun 2021 19:41:22 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Sun, 27 Jun 2021 19:41:26 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Sun, 27 Jun 2021 19:41:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Sun, 27 Jun 2021 19:41:36 GMT
VOLUME [/var/lib/eg]
# Sun, 27 Jun 2021 19:41:40 GMT
EXPOSE 8080 9876
# Sun, 27 Jun 2021 19:41:44 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Sun, 27 Jun 2021 19:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 19:41:55 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:3be5611c0e64110909576b6b123a979626cbd064adb316722e45cebf5429ba51`  
		Last Modified: Wed, 14 Apr 2021 19:33:01 GMT  
		Size: 2.8 MB (2823734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bbd7a57bf45662270e7a86ebda57e981d07009529d9415c5ab6edb6916e6e1`  
		Last Modified: Sun, 27 Jun 2021 04:17:16 GMT  
		Size: 26.9 MB (26885597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f06e577e6e46168a31d1062509799d0d4378836bfc7ed69cc7d58ec0e3984d`  
		Last Modified: Sun, 27 Jun 2021 04:17:11 GMT  
		Size: 2.3 MB (2296917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd49437458087223d0c7e45c42bb1fac7f674b614135b908bc81ab7e5bfa37b`  
		Last Modified: Sun, 27 Jun 2021 04:17:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a63fb2c906dff6e0372a6fb36a267af33a6f6f838e7053e8d0d0649f1b297bd`  
		Last Modified: Sun, 27 Jun 2021 19:42:21 GMT  
		Size: 9.9 MB (9898657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1505c4888e140d303da5c76397170ed4c70cd24f9426f17a355db51c856ee8c5`  
		Last Modified: Sun, 27 Jun 2021 19:42:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; s390x

```console
$ docker pull express-gateway@sha256:11add88677afc864d02ffbac3b1529ded61d5dab95bc4179419a73a614170d7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39424451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223f1c874f82ab8a0aced01f13ce74dd0c0e0f92d1cdc9b80dfc4cc06940d05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:48 GMT
ADD file:f01bbceaff31cff54d8147154b6fc2938fd2d9866e90147689bd0b2c39e3ba5f in / 
# Wed, 14 Apr 2021 18:41:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:38:55 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 05:01:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 05:02:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 05:02:09 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 05:02:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:02:11 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:50:16 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:50:16 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:50:39 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:50:41 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:50:42 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:50:42 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:50:42 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:50:42 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:50:43 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:50:43 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:50:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:50:44 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:01bec321d6f53c2537689093496de5b1b149c5f1b25b80c786c537b3e153dbb8`  
		Last Modified: Wed, 14 Apr 2021 18:42:32 GMT  
		Size: 2.6 MB (2584667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d693e481a9cbde501cc1e06670a6f86b34f6f79853bf8fdc541b834dc6d4a83`  
		Last Modified: Wed, 07 Jul 2021 05:35:01 GMT  
		Size: 24.6 MB (24638654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73c01ec51af6cb4229ac118c0b7b0d67ce31fdb2677a3014cea73cb1728ad`  
		Last Modified: Wed, 07 Jul 2021 05:34:58 GMT  
		Size: 2.3 MB (2301691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed5f847e806f775a1b283645005c9770655edd8b79b7b218b84c2c72f2df0b5`  
		Last Modified: Wed, 07 Jul 2021 05:34:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3341322fc9e42c6b702520ede0f63ff227f7a3f41a1cebc93cb95c936e67bc27`  
		Last Modified: Wed, 07 Jul 2021 05:51:07 GMT  
		Size: 9.9 MB (9898658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462f2601717e3efc30e1c4e6261686ee5513c1d4f36a10f3aa2faa89849213e5`  
		Last Modified: Wed, 07 Jul 2021 05:51:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:1.x`

```console
$ docker pull express-gateway@sha256:367d4ac9dbd77a44b280e66d80be62697431a5ed87686c916283b8797845945a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.x` - linux; amd64

```console
$ docker pull express-gateway@sha256:b1bad91f6d5a13e41a48d1ec8ecdd6b7e19beec82442f90a008f67a7a8b3921c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39556032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dc911ce70e6d71e8f133d9bbdaf7dcc75893568429420b58a5849150ee0f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:59:28 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 17:59:28 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 17:59:45 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 17:59:46 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 17:59:46 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 17:59:47 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 17:59:47 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 17:59:47 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:59:47 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fb847bc81fd2087a0ad97758300d091b6e92a43bcfc5546dbfd23f913e43b0`  
		Last Modified: Wed, 07 Jul 2021 18:00:05 GMT  
		Size: 9.9 MB (9898550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ecdcfd1afec27a31d62ada59ea53ec9f7cf82856a06e7af755b456a1b990a0`  
		Last Modified: Wed, 07 Jul 2021 18:00:02 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:76403d126c69fa2b67caafeeead58bc990e8b7ef6478820cba7750903729d489
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39654510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33bfd0aa6700ed5c58d3f45b35dd037639eff716ed1643d6f9acbb9cd4f51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:21:10 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 04:49:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 04:49:02 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 04:49:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 04:49:07 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 04:49:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 04:49:08 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:36:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:36:11 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:36:29 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:36:30 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:36:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:36:31 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:36:31 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:36:31 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:36:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:36:31 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea3779ab6047f8155b959727d18ea94cc5468e381fa4b6e589b41847bee610c`  
		Last Modified: Wed, 07 Jul 2021 05:33:10 GMT  
		Size: 24.7 MB (24729422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53cc19e504a9644d8a550e441c5f7c441eab66310bbfacb9bee0dc18a53572e`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 2.3 MB (2299356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2e06d2bdcce894629edb871383d5e50387496101290cbf487255746af66d4d`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926150d403084ea7fcd6c97c4e109769961ac9865e347b3be2471a49cca504a`  
		Last Modified: Wed, 07 Jul 2021 05:36:54 GMT  
		Size: 9.9 MB (9898027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c92afc4de53f859121fdc0cf49038122469b118b51a85fb82777c5820c2fe6e`  
		Last Modified: Wed, 07 Jul 2021 05:36:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:e876ffb4fc41c7ae5b37eb7b841356d0e5ac9e2ec68843cbe2914e6bc7b8a027
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41905682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dfcb2361e91576bef7b8021e64741af100c9f407600f4b87320b948e9e1113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:38 GMT
ADD file:91004afe9c028e9c999ada226de52c8f6a429c745e4dfe0502eab6e63fee09b1 in / 
# Wed, 14 Apr 2021 19:31:44 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 03:18:28 GMT
ENV NODE_VERSION=12.22.1
# Sun, 27 Jun 2021 03:37:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b7c8a2cb26790b4cc21a69ea5896ecb3e88712a35dcd5f3ef1c799214ad1f5da"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sun, 27 Jun 2021 03:37:14 GMT
ENV YARN_VERSION=1.22.5
# Sun, 27 Jun 2021 03:37:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sun, 27 Jun 2021 03:37:30 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 27 Jun 2021 03:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 03:37:51 GMT
CMD ["node"]
# Sun, 27 Jun 2021 19:39:53 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Sun, 27 Jun 2021 19:39:59 GMT
ARG EG_VERSION=1.16.11
# Sun, 27 Jun 2021 19:41:05 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Sun, 27 Jun 2021 19:41:15 GMT
ENV NODE_ENV=production
# Sun, 27 Jun 2021 19:41:22 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Sun, 27 Jun 2021 19:41:26 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Sun, 27 Jun 2021 19:41:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Sun, 27 Jun 2021 19:41:36 GMT
VOLUME [/var/lib/eg]
# Sun, 27 Jun 2021 19:41:40 GMT
EXPOSE 8080 9876
# Sun, 27 Jun 2021 19:41:44 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Sun, 27 Jun 2021 19:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 19:41:55 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:3be5611c0e64110909576b6b123a979626cbd064adb316722e45cebf5429ba51`  
		Last Modified: Wed, 14 Apr 2021 19:33:01 GMT  
		Size: 2.8 MB (2823734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bbd7a57bf45662270e7a86ebda57e981d07009529d9415c5ab6edb6916e6e1`  
		Last Modified: Sun, 27 Jun 2021 04:17:16 GMT  
		Size: 26.9 MB (26885597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f06e577e6e46168a31d1062509799d0d4378836bfc7ed69cc7d58ec0e3984d`  
		Last Modified: Sun, 27 Jun 2021 04:17:11 GMT  
		Size: 2.3 MB (2296917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd49437458087223d0c7e45c42bb1fac7f674b614135b908bc81ab7e5bfa37b`  
		Last Modified: Sun, 27 Jun 2021 04:17:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a63fb2c906dff6e0372a6fb36a267af33a6f6f838e7053e8d0d0649f1b297bd`  
		Last Modified: Sun, 27 Jun 2021 19:42:21 GMT  
		Size: 9.9 MB (9898657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1505c4888e140d303da5c76397170ed4c70cd24f9426f17a355db51c856ee8c5`  
		Last Modified: Sun, 27 Jun 2021 19:42:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; s390x

```console
$ docker pull express-gateway@sha256:11add88677afc864d02ffbac3b1529ded61d5dab95bc4179419a73a614170d7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39424451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223f1c874f82ab8a0aced01f13ce74dd0c0e0f92d1cdc9b80dfc4cc06940d05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:48 GMT
ADD file:f01bbceaff31cff54d8147154b6fc2938fd2d9866e90147689bd0b2c39e3ba5f in / 
# Wed, 14 Apr 2021 18:41:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:38:55 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 05:01:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 05:02:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 05:02:09 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 05:02:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:02:11 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:50:16 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:50:16 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:50:39 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:50:41 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:50:42 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:50:42 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:50:42 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:50:42 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:50:43 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:50:43 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:50:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:50:44 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:01bec321d6f53c2537689093496de5b1b149c5f1b25b80c786c537b3e153dbb8`  
		Last Modified: Wed, 14 Apr 2021 18:42:32 GMT  
		Size: 2.6 MB (2584667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d693e481a9cbde501cc1e06670a6f86b34f6f79853bf8fdc541b834dc6d4a83`  
		Last Modified: Wed, 07 Jul 2021 05:35:01 GMT  
		Size: 24.6 MB (24638654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73c01ec51af6cb4229ac118c0b7b0d67ce31fdb2677a3014cea73cb1728ad`  
		Last Modified: Wed, 07 Jul 2021 05:34:58 GMT  
		Size: 2.3 MB (2301691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed5f847e806f775a1b283645005c9770655edd8b79b7b218b84c2c72f2df0b5`  
		Last Modified: Wed, 07 Jul 2021 05:34:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3341322fc9e42c6b702520ede0f63ff227f7a3f41a1cebc93cb95c936e67bc27`  
		Last Modified: Wed, 07 Jul 2021 05:51:07 GMT  
		Size: 9.9 MB (9898658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462f2601717e3efc30e1c4e6261686ee5513c1d4f36a10f3aa2faa89849213e5`  
		Last Modified: Wed, 07 Jul 2021 05:51:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:latest`

```console
$ docker pull express-gateway@sha256:367d4ac9dbd77a44b280e66d80be62697431a5ed87686c916283b8797845945a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:latest` - linux; amd64

```console
$ docker pull express-gateway@sha256:b1bad91f6d5a13e41a48d1ec8ecdd6b7e19beec82442f90a008f67a7a8b3921c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39556032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dc911ce70e6d71e8f133d9bbdaf7dcc75893568429420b58a5849150ee0f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:59:28 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 17:59:28 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 17:59:45 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 17:59:46 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 17:59:46 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 17:59:46 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 17:59:47 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 17:59:47 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 17:59:47 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:59:47 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fb847bc81fd2087a0ad97758300d091b6e92a43bcfc5546dbfd23f913e43b0`  
		Last Modified: Wed, 07 Jul 2021 18:00:05 GMT  
		Size: 9.9 MB (9898550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ecdcfd1afec27a31d62ada59ea53ec9f7cf82856a06e7af755b456a1b990a0`  
		Last Modified: Wed, 07 Jul 2021 18:00:02 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:76403d126c69fa2b67caafeeead58bc990e8b7ef6478820cba7750903729d489
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39654510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33bfd0aa6700ed5c58d3f45b35dd037639eff716ed1643d6f9acbb9cd4f51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:21:10 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 04:49:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 04:49:02 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 04:49:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 04:49:07 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 04:49:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 04:49:08 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:36:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:36:11 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:36:29 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:36:30 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:36:30 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:36:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:36:31 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:36:31 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:36:31 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:36:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:36:31 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea3779ab6047f8155b959727d18ea94cc5468e381fa4b6e589b41847bee610c`  
		Last Modified: Wed, 07 Jul 2021 05:33:10 GMT  
		Size: 24.7 MB (24729422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53cc19e504a9644d8a550e441c5f7c441eab66310bbfacb9bee0dc18a53572e`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 2.3 MB (2299356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2e06d2bdcce894629edb871383d5e50387496101290cbf487255746af66d4d`  
		Last Modified: Wed, 07 Jul 2021 05:33:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926150d403084ea7fcd6c97c4e109769961ac9865e347b3be2471a49cca504a`  
		Last Modified: Wed, 07 Jul 2021 05:36:54 GMT  
		Size: 9.9 MB (9898027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c92afc4de53f859121fdc0cf49038122469b118b51a85fb82777c5820c2fe6e`  
		Last Modified: Wed, 07 Jul 2021 05:36:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:e876ffb4fc41c7ae5b37eb7b841356d0e5ac9e2ec68843cbe2914e6bc7b8a027
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41905682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dfcb2361e91576bef7b8021e64741af100c9f407600f4b87320b948e9e1113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:38 GMT
ADD file:91004afe9c028e9c999ada226de52c8f6a429c745e4dfe0502eab6e63fee09b1 in / 
# Wed, 14 Apr 2021 19:31:44 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 03:18:28 GMT
ENV NODE_VERSION=12.22.1
# Sun, 27 Jun 2021 03:37:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b7c8a2cb26790b4cc21a69ea5896ecb3e88712a35dcd5f3ef1c799214ad1f5da"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sun, 27 Jun 2021 03:37:14 GMT
ENV YARN_VERSION=1.22.5
# Sun, 27 Jun 2021 03:37:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sun, 27 Jun 2021 03:37:30 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 27 Jun 2021 03:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 03:37:51 GMT
CMD ["node"]
# Sun, 27 Jun 2021 19:39:53 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Sun, 27 Jun 2021 19:39:59 GMT
ARG EG_VERSION=1.16.11
# Sun, 27 Jun 2021 19:41:05 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Sun, 27 Jun 2021 19:41:15 GMT
ENV NODE_ENV=production
# Sun, 27 Jun 2021 19:41:22 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Sun, 27 Jun 2021 19:41:26 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Sun, 27 Jun 2021 19:41:30 GMT
ENV CHOKIDAR_USEPOLLING=true
# Sun, 27 Jun 2021 19:41:36 GMT
VOLUME [/var/lib/eg]
# Sun, 27 Jun 2021 19:41:40 GMT
EXPOSE 8080 9876
# Sun, 27 Jun 2021 19:41:44 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Sun, 27 Jun 2021 19:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 27 Jun 2021 19:41:55 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:3be5611c0e64110909576b6b123a979626cbd064adb316722e45cebf5429ba51`  
		Last Modified: Wed, 14 Apr 2021 19:33:01 GMT  
		Size: 2.8 MB (2823734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bbd7a57bf45662270e7a86ebda57e981d07009529d9415c5ab6edb6916e6e1`  
		Last Modified: Sun, 27 Jun 2021 04:17:16 GMT  
		Size: 26.9 MB (26885597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f06e577e6e46168a31d1062509799d0d4378836bfc7ed69cc7d58ec0e3984d`  
		Last Modified: Sun, 27 Jun 2021 04:17:11 GMT  
		Size: 2.3 MB (2296917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd49437458087223d0c7e45c42bb1fac7f674b614135b908bc81ab7e5bfa37b`  
		Last Modified: Sun, 27 Jun 2021 04:17:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a63fb2c906dff6e0372a6fb36a267af33a6f6f838e7053e8d0d0649f1b297bd`  
		Last Modified: Sun, 27 Jun 2021 19:42:21 GMT  
		Size: 9.9 MB (9898657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1505c4888e140d303da5c76397170ed4c70cd24f9426f17a355db51c856ee8c5`  
		Last Modified: Sun, 27 Jun 2021 19:42:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; s390x

```console
$ docker pull express-gateway@sha256:11add88677afc864d02ffbac3b1529ded61d5dab95bc4179419a73a614170d7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39424451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223f1c874f82ab8a0aced01f13ce74dd0c0e0f92d1cdc9b80dfc4cc06940d05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:48 GMT
ADD file:f01bbceaff31cff54d8147154b6fc2938fd2d9866e90147689bd0b2c39e3ba5f in / 
# Wed, 14 Apr 2021 18:41:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 04:38:55 GMT
ENV NODE_VERSION=12.22.2
# Wed, 07 Jul 2021 05:01:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="242bc6f948186d64be162ea7fd5c64fe15d5863100db0d0478ae8853533859c2"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 05:02:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 05:02:09 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 05:02:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:02:11 GMT
CMD ["node"]
# Wed, 07 Jul 2021 05:50:16 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 07 Jul 2021 05:50:16 GMT
ARG EG_VERSION=1.16.11
# Wed, 07 Jul 2021 05:50:39 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 07 Jul 2021 05:50:41 GMT
ENV NODE_ENV=production
# Wed, 07 Jul 2021 05:50:42 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 07 Jul 2021 05:50:42 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 07 Jul 2021 05:50:42 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 07 Jul 2021 05:50:42 GMT
VOLUME [/var/lib/eg]
# Wed, 07 Jul 2021 05:50:43 GMT
EXPOSE 8080 9876
# Wed, 07 Jul 2021 05:50:43 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 07 Jul 2021 05:50:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 05:50:44 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:01bec321d6f53c2537689093496de5b1b149c5f1b25b80c786c537b3e153dbb8`  
		Last Modified: Wed, 14 Apr 2021 18:42:32 GMT  
		Size: 2.6 MB (2584667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d693e481a9cbde501cc1e06670a6f86b34f6f79853bf8fdc541b834dc6d4a83`  
		Last Modified: Wed, 07 Jul 2021 05:35:01 GMT  
		Size: 24.6 MB (24638654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73c01ec51af6cb4229ac118c0b7b0d67ce31fdb2677a3014cea73cb1728ad`  
		Last Modified: Wed, 07 Jul 2021 05:34:58 GMT  
		Size: 2.3 MB (2301691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed5f847e806f775a1b283645005c9770655edd8b79b7b218b84c2c72f2df0b5`  
		Last Modified: Wed, 07 Jul 2021 05:34:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3341322fc9e42c6b702520ede0f63ff227f7a3f41a1cebc93cb95c936e67bc27`  
		Last Modified: Wed, 07 Jul 2021 05:51:07 GMT  
		Size: 9.9 MB (9898658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462f2601717e3efc30e1c4e6261686ee5513c1d4f36a10f3aa2faa89849213e5`  
		Last Modified: Wed, 07 Jul 2021 05:51:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

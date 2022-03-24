## `express-gateway:latest`

```console
$ docker pull express-gateway@sha256:fe2a7706074f8ed620615134f99885b2c99b17b3bb2e4e3ddf2668848fdc5ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:latest` - linux; amd64

```console
$ docker pull express-gateway@sha256:a56a0e384e1b298bd59e27982e45710024abc18621cb4ffcc2f5dab1245b26b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40212008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971090201c2ca3f1e893aa9cd026bf405e0d7bb80d8ed2109f5bf4d3e19a5b45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 15:36:48 GMT
ENV NODE_VERSION=12.22.11
# Wed, 23 Mar 2022 15:36:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c30c9ba214a8eb2db6199db9147f14ff2cbb0fc07e4517e3a8758f213cc71128"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 23 Mar 2022 15:36:55 GMT
ENV YARN_VERSION=1.22.17
# Wed, 23 Mar 2022 15:36:59 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 23 Mar 2022 15:36:59 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 23 Mar 2022 15:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 15:36:59 GMT
CMD ["node"]
# Wed, 23 Mar 2022 21:08:32 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 23 Mar 2022 21:08:32 GMT
ARG EG_VERSION=1.16.11
# Wed, 23 Mar 2022 21:08:49 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 23 Mar 2022 21:08:50 GMT
ENV NODE_ENV=production
# Wed, 23 Mar 2022 21:08:50 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 23 Mar 2022 21:08:50 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 23 Mar 2022 21:08:50 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 23 Mar 2022 21:08:50 GMT
VOLUME [/var/lib/eg]
# Wed, 23 Mar 2022 21:08:50 GMT
EXPOSE 8080 9876
# Wed, 23 Mar 2022 21:08:50 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 23 Mar 2022 21:08:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:08:50 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dccbde8d19e4e5685c480c38bb75c1acd314321af8e9539e1dc8a217c52a425`  
		Last Modified: Wed, 23 Mar 2022 15:45:35 GMT  
		Size: 24.9 MB (24908155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8993aed800098ec0e5f5ebb6cac42e8d342674483260a5eae30a0185f141704`  
		Last Modified: Wed, 23 Mar 2022 15:45:31 GMT  
		Size: 2.4 MB (2357844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa75fa02c7f47c4211467eb1af632e6e8adf7f774753d4aab5a8cee070a86bbc`  
		Last Modified: Wed, 23 Mar 2022 15:45:31 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e5fe444b21461ea6b8401b83123400441e991b0f3c04db266c0556e8a84f4b`  
		Last Modified: Wed, 23 Mar 2022 21:09:05 GMT  
		Size: 10.1 MB (10132365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb494d0b13fc82df64f325b77d22ae23a7f57690448be1fbb978c933c0db6`  
		Last Modified: Wed, 23 Mar 2022 21:09:03 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:e289da82fec68956e4f74254ae8d320bfe6e3d100c72cad9eb09fcaaba91365b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40093324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb74ecd9d36d1feee0dc494d29ffa9055036b72bc4c4eb46c1a6a062772ae63d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 04:15:37 GMT
ENV NODE_VERSION=12.22.11
# Thu, 24 Mar 2022 04:32:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c30c9ba214a8eb2db6199db9147f14ff2cbb0fc07e4517e3a8758f213cc71128"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 24 Mar 2022 04:32:49 GMT
ENV YARN_VERSION=1.22.17
# Thu, 24 Mar 2022 04:32:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 24 Mar 2022 04:32:58 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 24 Mar 2022 04:32:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 04:32:59 GMT
CMD ["node"]
# Thu, 24 Mar 2022 10:11:47 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 24 Mar 2022 10:11:48 GMT
ARG EG_VERSION=1.16.11
# Thu, 24 Mar 2022 10:12:06 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 24 Mar 2022 10:12:07 GMT
ENV NODE_ENV=production
# Thu, 24 Mar 2022 10:12:08 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 24 Mar 2022 10:12:09 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 24 Mar 2022 10:12:10 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 24 Mar 2022 10:12:11 GMT
VOLUME [/var/lib/eg]
# Thu, 24 Mar 2022 10:12:12 GMT
EXPOSE 8080 9876
# Thu, 24 Mar 2022 10:12:14 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 24 Mar 2022 10:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 10:12:15 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522fdbfb550f6fd3cdae371b7cb96b50ce76ecc918000b30f1c69fb8b3290d6e`  
		Last Modified: Thu, 24 Mar 2022 04:45:41 GMT  
		Size: 24.8 MB (24803924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa072b44de9f74aa9be0e7638663aa4667998e6555fe605f6067ce9eba6aa6cb`  
		Last Modified: Thu, 24 Mar 2022 04:45:37 GMT  
		Size: 2.4 MB (2438220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd93b7f60cc144eab6643ef036cc79283733e42fa417d3e492ebd52ca2a530c0`  
		Last Modified: Thu, 24 Mar 2022 04:45:36 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7b010c1120cf89b27c05d8ed35d837be7d7d559a0739eb77993a518fda4ebd`  
		Last Modified: Thu, 24 Mar 2022 10:12:38 GMT  
		Size: 10.1 MB (10135516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191b16e10d62e343f0931a67815a944e12b1c2fea1d6ce156eef341a463e0969`  
		Last Modified: Thu, 24 Mar 2022 10:12:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:a15467427545f611ca023d9d9c9b2fc910e69129a1444f872fd5f94bcc555815
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42523577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed69808c8164eb46c5149747a538f9658b20ab0d65b724d536734e1b7b02efb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:22:09 GMT
ENV NODE_VERSION=12.22.11
# Wed, 23 Mar 2022 18:42:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c30c9ba214a8eb2db6199db9147f14ff2cbb0fc07e4517e3a8758f213cc71128"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 23 Mar 2022 18:43:01 GMT
ENV YARN_VERSION=1.22.17
# Wed, 23 Mar 2022 18:43:17 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 23 Mar 2022 18:43:19 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 23 Mar 2022 18:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:43:28 GMT
CMD ["node"]
# Thu, 24 Mar 2022 03:19:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 24 Mar 2022 03:19:19 GMT
ARG EG_VERSION=1.16.11
# Thu, 24 Mar 2022 03:20:05 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 24 Mar 2022 03:20:10 GMT
ENV NODE_ENV=production
# Thu, 24 Mar 2022 03:20:12 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 24 Mar 2022 03:20:13 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 24 Mar 2022 03:20:14 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 24 Mar 2022 03:20:18 GMT
VOLUME [/var/lib/eg]
# Thu, 24 Mar 2022 03:20:21 GMT
EXPOSE 8080 9876
# Thu, 24 Mar 2022 03:20:22 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:20:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:20:27 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4575731fccba79ce6eeb2c43412d548f6dc43f4d2cdc630aa9cadeb40122037`  
		Last Modified: Wed, 23 Mar 2022 18:55:51 GMT  
		Size: 27.1 MB (27136194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d39f0bb4a69e28cb4a43e5ae41f93b227746be100da3469f2e22cd28f60c94a`  
		Last Modified: Wed, 23 Mar 2022 18:55:44 GMT  
		Size: 2.4 MB (2438354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f01c1d43850b2f0317f6b8d1908a039dc4350851a5001ddc82d66bd564560`  
		Last Modified: Wed, 23 Mar 2022 18:55:42 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d62bcd060b9eb828dab85d30c48fe9f688153c0fe472b8337f666d3ac076408`  
		Last Modified: Thu, 24 Mar 2022 03:20:53 GMT  
		Size: 10.1 MB (10134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0a31928c9a6140844fab68f95534c4697140e29b2e79fb9643fb79aa0bafa`  
		Last Modified: Thu, 24 Mar 2022 03:20:50 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; s390x

```console
$ docker pull express-gateway@sha256:f069453d4ee30bb8d6aa7217b93c872d8bfb35d60cc12d5a148b9498aaadf192
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39979144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0831c88498e3bd05a5be65c39ca2cc1602a07ca4bf4bec47f1a65a46aa7aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:01:56 GMT
ENV NODE_VERSION=12.22.11
# Wed, 23 Mar 2022 18:20:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="c30c9ba214a8eb2db6199db9147f14ff2cbb0fc07e4517e3a8758f213cc71128"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 23 Mar 2022 18:21:00 GMT
ENV YARN_VERSION=1.22.17
# Wed, 23 Mar 2022 18:21:04 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 23 Mar 2022 18:21:04 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 23 Mar 2022 18:21:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:21:04 GMT
CMD ["node"]
# Wed, 23 Mar 2022 22:14:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 23 Mar 2022 22:14:12 GMT
ARG EG_VERSION=1.16.11
# Wed, 23 Mar 2022 22:14:38 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 23 Mar 2022 22:14:43 GMT
ENV NODE_ENV=production
# Wed, 23 Mar 2022 22:14:44 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 23 Mar 2022 22:14:44 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 23 Mar 2022 22:14:44 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 23 Mar 2022 22:14:45 GMT
VOLUME [/var/lib/eg]
# Wed, 23 Mar 2022 22:14:45 GMT
EXPOSE 8080 9876
# Wed, 23 Mar 2022 22:14:46 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 22:14:47 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee56a1176e35d058d02a30ffb81df76a0467e3a142e963998687c546022e704`  
		Last Modified: Wed, 23 Mar 2022 18:30:15 GMT  
		Size: 24.8 MB (24802122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffc08882d1a3fbe154a54770cf2d098d44000c83d5c2e60dbacecf485684fbd`  
		Last Modified: Wed, 23 Mar 2022 18:30:12 GMT  
		Size: 2.4 MB (2440706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5724262b22b98575d239e3cfe7dd8a0c344919145c337b7bc733b1d7266fd517`  
		Last Modified: Wed, 23 Mar 2022 18:30:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999e00851364ea1777b44baf318d13f323e58169fbc377676058c70cd1e14cb6`  
		Last Modified: Wed, 23 Mar 2022 22:15:11 GMT  
		Size: 10.1 MB (10133672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b3dbab2c440a71ec06e992405a635f4998ff40a20fb3892ed06b90396606fc`  
		Last Modified: Wed, 23 Mar 2022 22:15:09 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

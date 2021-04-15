## `express-gateway:latest`

```console
$ docker pull express-gateway@sha256:856f11bd908e5743b1d84f6d7915005aa781f0acf87d69f67793ef9ecc3a2872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:latest` - linux; amd64

```console
$ docker pull express-gateway@sha256:c31738a712b65a8a322677c6beb1fcda10b8c6250855774b988eeb5ce5a7cc6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37327590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38d487b2a6222e792ddfa05ea257531ff9ca4bd8089f3a4b0c72279e6c39d03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:21:07 GMT
ENV NODE_VERSION=10.24.1
# Wed, 14 Apr 2021 23:21:12 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 14 Apr 2021 23:21:13 GMT
ENV YARN_VERSION=1.22.5
# Wed, 14 Apr 2021 23:21:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 14 Apr 2021 23:21:16 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 14 Apr 2021 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:21:16 GMT
CMD ["node"]
# Thu, 15 Apr 2021 09:54:25 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 15 Apr 2021 09:54:25 GMT
ARG EG_VERSION=1.16.10
# Thu, 15 Apr 2021 09:54:41 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 15 Apr 2021 09:54:42 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 09:54:42 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 15 Apr 2021 09:54:42 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 15 Apr 2021 09:54:42 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 15 Apr 2021 09:54:43 GMT
VOLUME [/var/lib/eg]
# Thu, 15 Apr 2021 09:54:43 GMT
EXPOSE 8080 9876
# Thu, 15 Apr 2021 09:54:43 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 09:54:43 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de915e575d22c7e33c83fddaf7aee0672e5d6a67e598a26fe0b30c7022f53cdd`  
		Last Modified: Wed, 14 Apr 2021 23:30:01 GMT  
		Size: 22.2 MB (22205881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7150aa69525b95f82b3df6a61a002f82382b2f3ea8ce51b9000b965f7476a5cc`  
		Last Modified: Wed, 14 Apr 2021 23:29:58 GMT  
		Size: 2.3 MB (2345009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aa47be044e5a988e3e7f204e2e28cb9f070daa32ed081072ad6d5bf6c085d1`  
		Last Modified: Wed, 14 Apr 2021 23:29:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a7f13c00f882309ef068711906179650745e59de15ce10301c9c9575789c6`  
		Last Modified: Thu, 15 Apr 2021 09:54:59 GMT  
		Size: 10.0 MB (9959672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbe03c10ed83715cda9d7c72bf01dce97b76e757b5b6f9c217dbde7d9c09450`  
		Last Modified: Thu, 15 Apr 2021 09:54:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:8555fdb66a0a06daf951a540a2039a59d1363892b28684b6da216be95bd0f137
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37560985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726ff5beee7385ffb35baf6bb7bc110dda52f3ecdd1fe09603779fbcd7651de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 04:12:22 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 04:18:34 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 04:18:35 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 04:18:40 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 04:18:41 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:18:43 GMT
CMD ["node"]
# Thu, 15 Apr 2021 10:32:56 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 15 Apr 2021 10:32:57 GMT
ARG EG_VERSION=1.16.10
# Thu, 15 Apr 2021 10:33:28 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 15 Apr 2021 10:33:31 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 10:33:32 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 15 Apr 2021 10:33:33 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 15 Apr 2021 10:33:33 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 15 Apr 2021 10:33:34 GMT
VOLUME [/var/lib/eg]
# Thu, 15 Apr 2021 10:33:35 GMT
EXPOSE 8080 9876
# Thu, 15 Apr 2021 10:33:36 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 15 Apr 2021 10:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 10:33:37 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c43cfd44af11f89b8167480c786154d3f0d370606cd156da69ff0cf0956389`  
		Last Modified: Thu, 15 Apr 2021 04:28:15 GMT  
		Size: 22.5 MB (22464277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8393b5d5144cfccccc5ef02a524cdbcfd5c73975f3f24c3206a2722963a78de`  
		Last Modified: Thu, 15 Apr 2021 04:28:09 GMT  
		Size: 2.4 MB (2408223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ac3ba0a17ce3f95f099f3b2217dd8a31a0430647d5524ad0032b525cefeb70`  
		Last Modified: Thu, 15 Apr 2021 04:28:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650b4ab9cdaa53010cba5cbae42d9d0a84f81c84f2f6fa210c6ed2d4d95d50b5`  
		Last Modified: Thu, 15 Apr 2021 10:33:57 GMT  
		Size: 10.0 MB (9960778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee2cf40eb736a038f8614beed48b7aa55d46b7127d305a6ff2b9ede8a7f4563`  
		Last Modified: Thu, 15 Apr 2021 10:33:54 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; 386

```console
$ docker pull express-gateway@sha256:097c5ed2eb98070047dc43ee8ee45a83a85956abdc1c6b54fc7dc63946643bd3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37578702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc605ad889f1cbd36f3118f3a25c83a8bb60542adee785c4b7c391bd289b8852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:42 GMT
ADD file:09db668d771495bb87e6b4c5fde70d7e786ab1efdc74e677aabfc1f91a9c6621 in / 
# Wed, 14 Apr 2021 18:38:42 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:42:12 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 03:08:12 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 03:08:13 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 03:08:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 03:08:17 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:08:17 GMT
CMD ["node"]
# Thu, 15 Apr 2021 08:27:32 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 15 Apr 2021 08:27:33 GMT
ARG EG_VERSION=1.16.10
# Thu, 15 Apr 2021 08:27:49 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 15 Apr 2021 08:27:49 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 08:27:49 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 15 Apr 2021 08:27:50 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 15 Apr 2021 08:27:50 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 15 Apr 2021 08:27:50 GMT
VOLUME [/var/lib/eg]
# Thu, 15 Apr 2021 08:27:50 GMT
EXPOSE 8080 9876
# Thu, 15 Apr 2021 08:27:50 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 15 Apr 2021 08:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:27:51 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ac056f5820900a5fb1267696349da84ea69194da83f527e904b0f9c277c5f65d`  
		Last Modified: Wed, 14 Apr 2021 18:39:56 GMT  
		Size: 2.8 MB (2812104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bf833cba7798f71d74ca35e3912118596c737a57612328c013af2061e893c7`  
		Last Modified: Thu, 15 Apr 2021 03:09:56 GMT  
		Size: 22.4 MB (22437666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99650daa1a4d3f089856f37707f966da9830b4443381784ee942e89ae59d78`  
		Last Modified: Thu, 15 Apr 2021 03:09:51 GMT  
		Size: 2.4 MB (2368250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a40b59e62a8c55854a56d834fa68e444cc37851998fa95dda3b0912f13fe18a`  
		Last Modified: Thu, 15 Apr 2021 03:09:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b982352199ea7f49fc6924f2ce538c3a2a967b048f96d5d3c7e80fa1cc210b0`  
		Last Modified: Thu, 15 Apr 2021 08:28:13 GMT  
		Size: 10.0 MB (9959905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e9db974f03f087a720658d0f184357aea8667ccb41acbd93a6f2774a2d2af5`  
		Last Modified: Thu, 15 Apr 2021 08:28:10 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:b3cd891d9bf7d770eb52fd904991cf0c55ce0d507a66ad2005a6a836aa323ab8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39388843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148bae1b7f826212bf8725ff131089ffe7b98ad13dc733550e452a76d74164d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:38 GMT
ADD file:91004afe9c028e9c999ada226de52c8f6a429c745e4dfe0502eab6e63fee09b1 in / 
# Wed, 14 Apr 2021 19:31:44 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:52:02 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 04:04:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 04:04:21 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 04:04:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 04:04:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:04:40 GMT
CMD ["node"]
# Thu, 15 Apr 2021 10:46:41 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 15 Apr 2021 10:46:47 GMT
ARG EG_VERSION=1.16.10
# Thu, 15 Apr 2021 10:47:54 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 15 Apr 2021 10:48:02 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 10:48:08 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 15 Apr 2021 10:48:12 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 15 Apr 2021 10:48:17 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 15 Apr 2021 10:48:24 GMT
VOLUME [/var/lib/eg]
# Thu, 15 Apr 2021 10:48:34 GMT
EXPOSE 8080 9876
# Thu, 15 Apr 2021 10:48:39 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 15 Apr 2021 10:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 10:48:49 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:3be5611c0e64110909576b6b123a979626cbd064adb316722e45cebf5429ba51`  
		Last Modified: Wed, 14 Apr 2021 19:33:01 GMT  
		Size: 2.8 MB (2823734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3793cecb4461f5726ce5a75a7511a4109aeb98f9d25b0b91c38a41bc69c982`  
		Last Modified: Thu, 15 Apr 2021 04:14:52 GMT  
		Size: 24.2 MB (24194545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738d6eff4e78f4b73b4b5a91a205013ff4bfbe3d16cf79c17963953b211bfacc`  
		Last Modified: Thu, 15 Apr 2021 04:14:47 GMT  
		Size: 2.4 MB (2408210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635c8fd04fbe9856fd356d56d78f218d42fc5ec755658f228785d4586b9c6318`  
		Last Modified: Thu, 15 Apr 2021 04:14:46 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2d68dd497cdf1487c88125be0007221663af7c75146cf350bfb9527f9bd80`  
		Last Modified: Thu, 15 Apr 2021 10:49:17 GMT  
		Size: 10.0 MB (9961573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc1273e8d4a30febccae0b29b84ade55f9621b19574275b45102f078f188333`  
		Last Modified: Thu, 15 Apr 2021 10:49:14 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; s390x

```console
$ docker pull express-gateway@sha256:3ff81ce8e6e3811e701ec753b6a1572134b48f535e0d8ced76cf7bb15a59c820
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37205995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e01cd57b2b08f99dbd077f994e7979aa8cd31df883366fdcc4f3d8b483d279`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:48 GMT
ADD file:f01bbceaff31cff54d8147154b6fc2938fd2d9866e90147689bd0b2c39e3ba5f in / 
# Wed, 14 Apr 2021 18:41:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:13:06 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 02:28:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 02:28:14 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 02:28:17 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 02:28:18 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:28:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:28:19 GMT
CMD ["node"]
# Thu, 15 Apr 2021 08:50:54 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 15 Apr 2021 08:50:55 GMT
ARG EG_VERSION=1.16.10
# Thu, 15 Apr 2021 08:51:35 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 15 Apr 2021 08:51:41 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 08:51:41 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 15 Apr 2021 08:51:42 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 15 Apr 2021 08:51:42 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 15 Apr 2021 08:51:43 GMT
VOLUME [/var/lib/eg]
# Thu, 15 Apr 2021 08:51:43 GMT
EXPOSE 8080 9876
# Thu, 15 Apr 2021 08:51:44 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 15 Apr 2021 08:51:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:51:45 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:01bec321d6f53c2537689093496de5b1b149c5f1b25b80c786c537b3e153dbb8`  
		Last Modified: Wed, 14 Apr 2021 18:42:32 GMT  
		Size: 2.6 MB (2584667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9420792836aae9b136e21c76ac20b6998745a22f10d70007b60d633f778df8b`  
		Last Modified: Thu, 15 Apr 2021 02:33:27 GMT  
		Size: 22.3 MB (22256047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847260b0fdc1242161276e8dc5310a2b6b28518f36798fbb4e911233cfd68e3f`  
		Last Modified: Thu, 15 Apr 2021 02:33:24 GMT  
		Size: 2.4 MB (2403459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415a1da688a7d744234d62f9b46eaee7d1f10bca51bf3d806667d0f67a52d60a`  
		Last Modified: Thu, 15 Apr 2021 02:33:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5bcffc56bfba89cf51219c3ab2137ea7dfdf00b8f2c18e93e205e3a4fe33ae`  
		Last Modified: Thu, 15 Apr 2021 08:52:02 GMT  
		Size: 10.0 MB (9961043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b096c6f62c127c92435fcf2b44c7fec1e3940cbc3ada00d3178ee4943652b9f`  
		Last Modified: Thu, 15 Apr 2021 08:52:00 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

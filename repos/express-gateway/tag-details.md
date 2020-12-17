<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `express-gateway`

-	[`express-gateway:1.16.10`](#express-gateway11610)
-	[`express-gateway:1.16.x`](#express-gateway116x)
-	[`express-gateway:1.x`](#express-gateway1x)
-	[`express-gateway:latest`](#express-gatewaylatest)

## `express-gateway:1.16.10`

```console
$ docker pull express-gateway@sha256:758c4b66651c975a65712ee88c47eaea837ca1ab25ca97c31ea2f29488db63ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.16.10` - linux; amd64

```console
$ docker pull express-gateway@sha256:cd76254212a5ef715fcf510c21256f39b395ef10e5371d651a1f0ef0a796fc05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37989012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ab8c2f75fa1e996b6b55dbee76e6b74879ab8d031a87925abd16ce96d3c62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:37:44 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 00:37:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 00:37:49 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 00:37:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 00:37:52 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 00:37:52 GMT
CMD ["node"]
# Wed, 28 Oct 2020 01:21:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 01:21:13 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 01:21:54 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 01:21:55 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 01:21:56 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 01:21:56 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 01:21:56 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 01:21:57 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 01:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 01:21:58 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38b11cdc566fe39a6feebbb0560b13b0c4ec0c2b20fc1959e06618f380ebf7`  
		Last Modified: Wed, 28 Oct 2020 00:46:54 GMT  
		Size: 22.5 MB (22458898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70377bd3b7462785e5ffc2ed4d37625d05a77c4a2cb81512a3384a4a54bd2b1c`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 2.3 MB (2344977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c0bc3a37c84a0326222e1b09a3d44501dd3c4eda61273636651cf13eba57`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1fb91b247cfc17bc416453741557544c0e431a6523166d277138d77dbfec99`  
		Last Modified: Wed, 28 Oct 2020 01:22:18 GMT  
		Size: 10.4 MB (10371039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92a8910d01ece7b23e329955fe0dcaa4fb25bf2d455fcc19ee9f459bcdce60`  
		Last Modified: Wed, 28 Oct 2020 01:22:13 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.10` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:2fa83656140da9d0fefcb7f94d5cc01679aa51537393c39b894b864cfd289ad7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38164799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f28a4f302c5fbdf42c0e2f1d15982b8fe2ab17ca00c8b660bc83f8ba5cb4563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:43:52 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:51:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:51:50 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:51:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:51:57 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:51:58 GMT
CMD ["node"]
# Thu, 17 Dec 2020 10:58:01 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 10:58:02 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 10:58:31 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 10:58:33 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 10:58:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 10:58:35 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 10:58:36 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 10:58:36 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 10:58:37 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 10:58:38 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 10:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 10:58:39 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc51f76858a2bdf99f2ca046c78849a1bc026e7277fad7b33ac8407b059a83`  
		Last Modified: Thu, 17 Dec 2020 03:59:31 GMT  
		Size: 22.7 MB (22714569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c9a78c1ec5f48a56201a42f2108b8f8a83cfa3d76e3865f8a0589b14171db3`  
		Last Modified: Thu, 17 Dec 2020 03:59:23 GMT  
		Size: 2.4 MB (2403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad951e768db1398a1e9d1a94bb1bdadcd55b20dbbab5e773522168c8503ba34`  
		Last Modified: Thu, 17 Dec 2020 03:59:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89002435d956e1557f411c11a562fc6b670582cf612b287df625af860e33ae62`  
		Last Modified: Thu, 17 Dec 2020 10:59:03 GMT  
		Size: 10.3 MB (10320650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b68f55df2a970e57dc6a00cfae05a1f7a833eb867a5381e4d92fb9a440cfcf8`  
		Last Modified: Thu, 17 Dec 2020 10:58:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.10` - linux; 386

```console
$ docker pull express-gateway@sha256:c9cb6e38a97c7ff7cc6199588a0f906dee1ba85ea94c04d1facbe4759fb3649f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8fef8170b13e6567e1edc0f8bb097b8d0c4601b6c19b6de1f1d8d4af38642d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:39 GMT
ADD file:c8f5b26cfa9b90dfe6ca805f2101bd199c87b93faed2af74df0cbe54ea28fa6d in / 
# Thu, 17 Dec 2020 00:38:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:02:10 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:31:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:31:17 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:31:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:31:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:31:21 GMT
CMD ["node"]
# Thu, 17 Dec 2020 08:48:23 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 08:48:23 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 08:48:49 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 08:48:50 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 08:48:50 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 08:48:50 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 08:48:50 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 08:48:50 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 08:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 08:48:51 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:60519712d04c07db59906a2e14fa87c037b6504d612ba116ea1ef94ae08a650b`  
		Last Modified: Thu, 17 Dec 2020 00:39:32 GMT  
		Size: 2.8 MB (2810512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f36a347448a466b18b94dc3e95cab6f5e09ebf07a01ce0f700b38313e503797`  
		Last Modified: Thu, 17 Dec 2020 03:32:12 GMT  
		Size: 22.7 MB (22691122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164d2c5829f7da75702be63355d41c7f3436defede5620d02ad36ca9ae9f847e`  
		Last Modified: Thu, 17 Dec 2020 03:32:06 GMT  
		Size: 2.4 MB (2364286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1609a84c1b04bf2fd9f8e56c5ac7d8a8773173bf6c24946c64a32aa8ebc68b25`  
		Last Modified: Thu, 17 Dec 2020 03:32:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fb2291d38d36981d4ae67e7f4019a7ace5a88d55ed6c89e400456e4167d82f`  
		Last Modified: Thu, 17 Dec 2020 08:49:08 GMT  
		Size: 10.3 MB (10321292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ae5bbc372d044bacfadc24bb46022e8f8b66a61a43ad5461393fb0176640ef`  
		Last Modified: Thu, 17 Dec 2020 08:49:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.10` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:607107e5af6a25e07e97e9c5e28daf5944b2363f12289e66e5d62ff2df3d00a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40037900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f989a954bc276a8c09aa56f1dc9c7661cb7c07544212bea8c41db2331462a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 02:02:01 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 02:17:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 02:17:38 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 02:18:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 02:18:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 02:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 02:18:10 GMT
CMD ["node"]
# Wed, 28 Oct 2020 03:22:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 03:22:17 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 03:22:53 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 03:22:58 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 03:23:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 03:23:07 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 03:23:11 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 03:23:14 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 03:23:17 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 03:23:19 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 03:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 03:23:27 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cf90450daa2d6b1b9cef450ab59c5cd7e844ee5787a4445eb8219e6554ad9c`  
		Last Modified: Wed, 28 Oct 2020 02:44:46 GMT  
		Size: 24.4 MB (24441894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401705d0a055c4c81009152ac255870e16555753cfa8b93e36cc1664d7eb478b`  
		Last Modified: Wed, 28 Oct 2020 02:44:41 GMT  
		Size: 2.4 MB (2403283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd907dddb2a9087a416892896a286c062b3edb82535a7c57d68ed458fa33b`  
		Last Modified: Wed, 28 Oct 2020 02:44:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a627da8d61d27e5bfd4ed08709dcf284498d3558dc59d58749c5658233bde9d8`  
		Last Modified: Wed, 28 Oct 2020 03:23:48 GMT  
		Size: 10.4 MB (10370098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0e0f877eb276a3f2daa2e390f668f6c9f32889b91b707664519d122858c34`  
		Last Modified: Wed, 28 Oct 2020 03:23:45 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.10` - linux; s390x

```console
$ docker pull express-gateway@sha256:b4f436da198547000c6943edbf71fbe6ccbe537ed4bc57594e43f21f69466498
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37818086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1163f758cb0b7723fa4c1c145e5043c73b54469aa054f704832cf46f7923370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:44 GMT
ADD file:9e0a7f4c5f520dabbf66a5d4312ceeb614fc5073fca7a248eb070cd99f4b75ff in / 
# Wed, 16 Dec 2020 23:41:44 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 05:26:06 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 05:46:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 05:46:09 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 05:46:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 05:46:15 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 05:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 05:46:16 GMT
CMD ["node"]
# Thu, 17 Dec 2020 11:57:17 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 11:57:18 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 11:57:56 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 11:58:02 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 11:58:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 11:58:03 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 11:58:04 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 11:58:04 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 11:58:05 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 11:58:05 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 11:58:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 11:58:07 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ae4c90d25da4580c1cd02a35a672d9113b17e063183b4148c463df4d33079192`  
		Last Modified: Wed, 16 Dec 2020 23:42:26 GMT  
		Size: 2.6 MB (2583287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22088d51a74c158f69cd817ecf9d4277da8bbf03cd3a1f6e4750bfa1895d2761`  
		Last Modified: Thu, 17 Dec 2020 05:50:56 GMT  
		Size: 22.5 MB (22512516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efadf5471afbfdd473e2f6e15ad368d4c74abf4ab424836ca8cc2ce4330a98c`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 2.4 MB (2400163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d69e94aa00bb65f0ad917a08bf596ae7f8361f7c360e34cd98fa90ed419083`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f270cb5c8c3d0cdadf24f76514671b1ce674d550cf9d61be869bbb6e4eacb`  
		Last Modified: Thu, 17 Dec 2020 11:58:22 GMT  
		Size: 10.3 MB (10321344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee80b5bfd57041b4d925714bdec268eb008a9db6edc49c14709336600df8a0c5`  
		Last Modified: Thu, 17 Dec 2020 11:58:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:1.16.x`

```console
$ docker pull express-gateway@sha256:758c4b66651c975a65712ee88c47eaea837ca1ab25ca97c31ea2f29488db63ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.16.x` - linux; amd64

```console
$ docker pull express-gateway@sha256:cd76254212a5ef715fcf510c21256f39b395ef10e5371d651a1f0ef0a796fc05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37989012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ab8c2f75fa1e996b6b55dbee76e6b74879ab8d031a87925abd16ce96d3c62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:37:44 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 00:37:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 00:37:49 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 00:37:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 00:37:52 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 00:37:52 GMT
CMD ["node"]
# Wed, 28 Oct 2020 01:21:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 01:21:13 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 01:21:54 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 01:21:55 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 01:21:56 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 01:21:56 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 01:21:56 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 01:21:57 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 01:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 01:21:58 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38b11cdc566fe39a6feebbb0560b13b0c4ec0c2b20fc1959e06618f380ebf7`  
		Last Modified: Wed, 28 Oct 2020 00:46:54 GMT  
		Size: 22.5 MB (22458898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70377bd3b7462785e5ffc2ed4d37625d05a77c4a2cb81512a3384a4a54bd2b1c`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 2.3 MB (2344977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c0bc3a37c84a0326222e1b09a3d44501dd3c4eda61273636651cf13eba57`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1fb91b247cfc17bc416453741557544c0e431a6523166d277138d77dbfec99`  
		Last Modified: Wed, 28 Oct 2020 01:22:18 GMT  
		Size: 10.4 MB (10371039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92a8910d01ece7b23e329955fe0dcaa4fb25bf2d455fcc19ee9f459bcdce60`  
		Last Modified: Wed, 28 Oct 2020 01:22:13 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:2fa83656140da9d0fefcb7f94d5cc01679aa51537393c39b894b864cfd289ad7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38164799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f28a4f302c5fbdf42c0e2f1d15982b8fe2ab17ca00c8b660bc83f8ba5cb4563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:43:52 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:51:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:51:50 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:51:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:51:57 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:51:58 GMT
CMD ["node"]
# Thu, 17 Dec 2020 10:58:01 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 10:58:02 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 10:58:31 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 10:58:33 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 10:58:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 10:58:35 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 10:58:36 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 10:58:36 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 10:58:37 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 10:58:38 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 10:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 10:58:39 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc51f76858a2bdf99f2ca046c78849a1bc026e7277fad7b33ac8407b059a83`  
		Last Modified: Thu, 17 Dec 2020 03:59:31 GMT  
		Size: 22.7 MB (22714569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c9a78c1ec5f48a56201a42f2108b8f8a83cfa3d76e3865f8a0589b14171db3`  
		Last Modified: Thu, 17 Dec 2020 03:59:23 GMT  
		Size: 2.4 MB (2403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad951e768db1398a1e9d1a94bb1bdadcd55b20dbbab5e773522168c8503ba34`  
		Last Modified: Thu, 17 Dec 2020 03:59:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89002435d956e1557f411c11a562fc6b670582cf612b287df625af860e33ae62`  
		Last Modified: Thu, 17 Dec 2020 10:59:03 GMT  
		Size: 10.3 MB (10320650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b68f55df2a970e57dc6a00cfae05a1f7a833eb867a5381e4d92fb9a440cfcf8`  
		Last Modified: Thu, 17 Dec 2020 10:58:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; 386

```console
$ docker pull express-gateway@sha256:c9cb6e38a97c7ff7cc6199588a0f906dee1ba85ea94c04d1facbe4759fb3649f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8fef8170b13e6567e1edc0f8bb097b8d0c4601b6c19b6de1f1d8d4af38642d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:39 GMT
ADD file:c8f5b26cfa9b90dfe6ca805f2101bd199c87b93faed2af74df0cbe54ea28fa6d in / 
# Thu, 17 Dec 2020 00:38:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:02:10 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:31:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:31:17 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:31:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:31:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:31:21 GMT
CMD ["node"]
# Thu, 17 Dec 2020 08:48:23 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 08:48:23 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 08:48:49 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 08:48:50 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 08:48:50 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 08:48:50 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 08:48:50 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 08:48:50 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 08:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 08:48:51 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:60519712d04c07db59906a2e14fa87c037b6504d612ba116ea1ef94ae08a650b`  
		Last Modified: Thu, 17 Dec 2020 00:39:32 GMT  
		Size: 2.8 MB (2810512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f36a347448a466b18b94dc3e95cab6f5e09ebf07a01ce0f700b38313e503797`  
		Last Modified: Thu, 17 Dec 2020 03:32:12 GMT  
		Size: 22.7 MB (22691122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164d2c5829f7da75702be63355d41c7f3436defede5620d02ad36ca9ae9f847e`  
		Last Modified: Thu, 17 Dec 2020 03:32:06 GMT  
		Size: 2.4 MB (2364286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1609a84c1b04bf2fd9f8e56c5ac7d8a8773173bf6c24946c64a32aa8ebc68b25`  
		Last Modified: Thu, 17 Dec 2020 03:32:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fb2291d38d36981d4ae67e7f4019a7ace5a88d55ed6c89e400456e4167d82f`  
		Last Modified: Thu, 17 Dec 2020 08:49:08 GMT  
		Size: 10.3 MB (10321292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ae5bbc372d044bacfadc24bb46022e8f8b66a61a43ad5461393fb0176640ef`  
		Last Modified: Thu, 17 Dec 2020 08:49:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:607107e5af6a25e07e97e9c5e28daf5944b2363f12289e66e5d62ff2df3d00a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40037900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f989a954bc276a8c09aa56f1dc9c7661cb7c07544212bea8c41db2331462a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 02:02:01 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 02:17:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 02:17:38 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 02:18:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 02:18:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 02:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 02:18:10 GMT
CMD ["node"]
# Wed, 28 Oct 2020 03:22:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 03:22:17 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 03:22:53 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 03:22:58 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 03:23:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 03:23:07 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 03:23:11 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 03:23:14 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 03:23:17 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 03:23:19 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 03:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 03:23:27 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cf90450daa2d6b1b9cef450ab59c5cd7e844ee5787a4445eb8219e6554ad9c`  
		Last Modified: Wed, 28 Oct 2020 02:44:46 GMT  
		Size: 24.4 MB (24441894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401705d0a055c4c81009152ac255870e16555753cfa8b93e36cc1664d7eb478b`  
		Last Modified: Wed, 28 Oct 2020 02:44:41 GMT  
		Size: 2.4 MB (2403283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd907dddb2a9087a416892896a286c062b3edb82535a7c57d68ed458fa33b`  
		Last Modified: Wed, 28 Oct 2020 02:44:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a627da8d61d27e5bfd4ed08709dcf284498d3558dc59d58749c5658233bde9d8`  
		Last Modified: Wed, 28 Oct 2020 03:23:48 GMT  
		Size: 10.4 MB (10370098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0e0f877eb276a3f2daa2e390f668f6c9f32889b91b707664519d122858c34`  
		Last Modified: Wed, 28 Oct 2020 03:23:45 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; s390x

```console
$ docker pull express-gateway@sha256:b4f436da198547000c6943edbf71fbe6ccbe537ed4bc57594e43f21f69466498
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37818086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1163f758cb0b7723fa4c1c145e5043c73b54469aa054f704832cf46f7923370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:44 GMT
ADD file:9e0a7f4c5f520dabbf66a5d4312ceeb614fc5073fca7a248eb070cd99f4b75ff in / 
# Wed, 16 Dec 2020 23:41:44 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 05:26:06 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 05:46:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 05:46:09 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 05:46:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 05:46:15 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 05:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 05:46:16 GMT
CMD ["node"]
# Thu, 17 Dec 2020 11:57:17 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 11:57:18 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 11:57:56 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 11:58:02 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 11:58:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 11:58:03 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 11:58:04 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 11:58:04 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 11:58:05 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 11:58:05 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 11:58:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 11:58:07 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ae4c90d25da4580c1cd02a35a672d9113b17e063183b4148c463df4d33079192`  
		Last Modified: Wed, 16 Dec 2020 23:42:26 GMT  
		Size: 2.6 MB (2583287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22088d51a74c158f69cd817ecf9d4277da8bbf03cd3a1f6e4750bfa1895d2761`  
		Last Modified: Thu, 17 Dec 2020 05:50:56 GMT  
		Size: 22.5 MB (22512516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efadf5471afbfdd473e2f6e15ad368d4c74abf4ab424836ca8cc2ce4330a98c`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 2.4 MB (2400163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d69e94aa00bb65f0ad917a08bf596ae7f8361f7c360e34cd98fa90ed419083`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f270cb5c8c3d0cdadf24f76514671b1ce674d550cf9d61be869bbb6e4eacb`  
		Last Modified: Thu, 17 Dec 2020 11:58:22 GMT  
		Size: 10.3 MB (10321344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee80b5bfd57041b4d925714bdec268eb008a9db6edc49c14709336600df8a0c5`  
		Last Modified: Thu, 17 Dec 2020 11:58:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:1.x`

```console
$ docker pull express-gateway@sha256:758c4b66651c975a65712ee88c47eaea837ca1ab25ca97c31ea2f29488db63ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.x` - linux; amd64

```console
$ docker pull express-gateway@sha256:cd76254212a5ef715fcf510c21256f39b395ef10e5371d651a1f0ef0a796fc05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37989012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ab8c2f75fa1e996b6b55dbee76e6b74879ab8d031a87925abd16ce96d3c62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:37:44 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 00:37:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 00:37:49 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 00:37:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 00:37:52 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 00:37:52 GMT
CMD ["node"]
# Wed, 28 Oct 2020 01:21:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 01:21:13 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 01:21:54 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 01:21:55 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 01:21:56 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 01:21:56 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 01:21:56 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 01:21:57 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 01:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 01:21:58 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38b11cdc566fe39a6feebbb0560b13b0c4ec0c2b20fc1959e06618f380ebf7`  
		Last Modified: Wed, 28 Oct 2020 00:46:54 GMT  
		Size: 22.5 MB (22458898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70377bd3b7462785e5ffc2ed4d37625d05a77c4a2cb81512a3384a4a54bd2b1c`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 2.3 MB (2344977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c0bc3a37c84a0326222e1b09a3d44501dd3c4eda61273636651cf13eba57`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1fb91b247cfc17bc416453741557544c0e431a6523166d277138d77dbfec99`  
		Last Modified: Wed, 28 Oct 2020 01:22:18 GMT  
		Size: 10.4 MB (10371039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92a8910d01ece7b23e329955fe0dcaa4fb25bf2d455fcc19ee9f459bcdce60`  
		Last Modified: Wed, 28 Oct 2020 01:22:13 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:2fa83656140da9d0fefcb7f94d5cc01679aa51537393c39b894b864cfd289ad7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38164799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f28a4f302c5fbdf42c0e2f1d15982b8fe2ab17ca00c8b660bc83f8ba5cb4563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:43:52 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:51:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:51:50 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:51:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:51:57 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:51:58 GMT
CMD ["node"]
# Thu, 17 Dec 2020 10:58:01 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 10:58:02 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 10:58:31 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 10:58:33 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 10:58:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 10:58:35 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 10:58:36 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 10:58:36 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 10:58:37 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 10:58:38 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 10:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 10:58:39 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc51f76858a2bdf99f2ca046c78849a1bc026e7277fad7b33ac8407b059a83`  
		Last Modified: Thu, 17 Dec 2020 03:59:31 GMT  
		Size: 22.7 MB (22714569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c9a78c1ec5f48a56201a42f2108b8f8a83cfa3d76e3865f8a0589b14171db3`  
		Last Modified: Thu, 17 Dec 2020 03:59:23 GMT  
		Size: 2.4 MB (2403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad951e768db1398a1e9d1a94bb1bdadcd55b20dbbab5e773522168c8503ba34`  
		Last Modified: Thu, 17 Dec 2020 03:59:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89002435d956e1557f411c11a562fc6b670582cf612b287df625af860e33ae62`  
		Last Modified: Thu, 17 Dec 2020 10:59:03 GMT  
		Size: 10.3 MB (10320650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b68f55df2a970e57dc6a00cfae05a1f7a833eb867a5381e4d92fb9a440cfcf8`  
		Last Modified: Thu, 17 Dec 2020 10:58:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; 386

```console
$ docker pull express-gateway@sha256:c9cb6e38a97c7ff7cc6199588a0f906dee1ba85ea94c04d1facbe4759fb3649f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8fef8170b13e6567e1edc0f8bb097b8d0c4601b6c19b6de1f1d8d4af38642d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:39 GMT
ADD file:c8f5b26cfa9b90dfe6ca805f2101bd199c87b93faed2af74df0cbe54ea28fa6d in / 
# Thu, 17 Dec 2020 00:38:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:02:10 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:31:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:31:17 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:31:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:31:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:31:21 GMT
CMD ["node"]
# Thu, 17 Dec 2020 08:48:23 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 08:48:23 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 08:48:49 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 08:48:50 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 08:48:50 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 08:48:50 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 08:48:50 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 08:48:50 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 08:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 08:48:51 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:60519712d04c07db59906a2e14fa87c037b6504d612ba116ea1ef94ae08a650b`  
		Last Modified: Thu, 17 Dec 2020 00:39:32 GMT  
		Size: 2.8 MB (2810512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f36a347448a466b18b94dc3e95cab6f5e09ebf07a01ce0f700b38313e503797`  
		Last Modified: Thu, 17 Dec 2020 03:32:12 GMT  
		Size: 22.7 MB (22691122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164d2c5829f7da75702be63355d41c7f3436defede5620d02ad36ca9ae9f847e`  
		Last Modified: Thu, 17 Dec 2020 03:32:06 GMT  
		Size: 2.4 MB (2364286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1609a84c1b04bf2fd9f8e56c5ac7d8a8773173bf6c24946c64a32aa8ebc68b25`  
		Last Modified: Thu, 17 Dec 2020 03:32:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fb2291d38d36981d4ae67e7f4019a7ace5a88d55ed6c89e400456e4167d82f`  
		Last Modified: Thu, 17 Dec 2020 08:49:08 GMT  
		Size: 10.3 MB (10321292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ae5bbc372d044bacfadc24bb46022e8f8b66a61a43ad5461393fb0176640ef`  
		Last Modified: Thu, 17 Dec 2020 08:49:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:607107e5af6a25e07e97e9c5e28daf5944b2363f12289e66e5d62ff2df3d00a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40037900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f989a954bc276a8c09aa56f1dc9c7661cb7c07544212bea8c41db2331462a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 02:02:01 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 02:17:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 02:17:38 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 02:18:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 02:18:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 02:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 02:18:10 GMT
CMD ["node"]
# Wed, 28 Oct 2020 03:22:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 03:22:17 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 03:22:53 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 03:22:58 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 03:23:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 03:23:07 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 03:23:11 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 03:23:14 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 03:23:17 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 03:23:19 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 03:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 03:23:27 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cf90450daa2d6b1b9cef450ab59c5cd7e844ee5787a4445eb8219e6554ad9c`  
		Last Modified: Wed, 28 Oct 2020 02:44:46 GMT  
		Size: 24.4 MB (24441894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401705d0a055c4c81009152ac255870e16555753cfa8b93e36cc1664d7eb478b`  
		Last Modified: Wed, 28 Oct 2020 02:44:41 GMT  
		Size: 2.4 MB (2403283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd907dddb2a9087a416892896a286c062b3edb82535a7c57d68ed458fa33b`  
		Last Modified: Wed, 28 Oct 2020 02:44:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a627da8d61d27e5bfd4ed08709dcf284498d3558dc59d58749c5658233bde9d8`  
		Last Modified: Wed, 28 Oct 2020 03:23:48 GMT  
		Size: 10.4 MB (10370098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0e0f877eb276a3f2daa2e390f668f6c9f32889b91b707664519d122858c34`  
		Last Modified: Wed, 28 Oct 2020 03:23:45 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; s390x

```console
$ docker pull express-gateway@sha256:b4f436da198547000c6943edbf71fbe6ccbe537ed4bc57594e43f21f69466498
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37818086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1163f758cb0b7723fa4c1c145e5043c73b54469aa054f704832cf46f7923370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:44 GMT
ADD file:9e0a7f4c5f520dabbf66a5d4312ceeb614fc5073fca7a248eb070cd99f4b75ff in / 
# Wed, 16 Dec 2020 23:41:44 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 05:26:06 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 05:46:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 05:46:09 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 05:46:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 05:46:15 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 05:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 05:46:16 GMT
CMD ["node"]
# Thu, 17 Dec 2020 11:57:17 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 11:57:18 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 11:57:56 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 11:58:02 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 11:58:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 11:58:03 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 11:58:04 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 11:58:04 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 11:58:05 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 11:58:05 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 11:58:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 11:58:07 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ae4c90d25da4580c1cd02a35a672d9113b17e063183b4148c463df4d33079192`  
		Last Modified: Wed, 16 Dec 2020 23:42:26 GMT  
		Size: 2.6 MB (2583287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22088d51a74c158f69cd817ecf9d4277da8bbf03cd3a1f6e4750bfa1895d2761`  
		Last Modified: Thu, 17 Dec 2020 05:50:56 GMT  
		Size: 22.5 MB (22512516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efadf5471afbfdd473e2f6e15ad368d4c74abf4ab424836ca8cc2ce4330a98c`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 2.4 MB (2400163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d69e94aa00bb65f0ad917a08bf596ae7f8361f7c360e34cd98fa90ed419083`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f270cb5c8c3d0cdadf24f76514671b1ce674d550cf9d61be869bbb6e4eacb`  
		Last Modified: Thu, 17 Dec 2020 11:58:22 GMT  
		Size: 10.3 MB (10321344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee80b5bfd57041b4d925714bdec268eb008a9db6edc49c14709336600df8a0c5`  
		Last Modified: Thu, 17 Dec 2020 11:58:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:latest`

```console
$ docker pull express-gateway@sha256:758c4b66651c975a65712ee88c47eaea837ca1ab25ca97c31ea2f29488db63ff
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
$ docker pull express-gateway@sha256:cd76254212a5ef715fcf510c21256f39b395ef10e5371d651a1f0ef0a796fc05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37989012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ab8c2f75fa1e996b6b55dbee76e6b74879ab8d031a87925abd16ce96d3c62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:37:44 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 00:37:49 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 00:37:49 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 00:37:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 00:37:52 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 00:37:52 GMT
CMD ["node"]
# Wed, 28 Oct 2020 01:21:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 01:21:13 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 01:21:54 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 01:21:55 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 01:21:55 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 01:21:56 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 01:21:56 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 01:21:56 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 01:21:57 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 01:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 01:21:58 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38b11cdc566fe39a6feebbb0560b13b0c4ec0c2b20fc1959e06618f380ebf7`  
		Last Modified: Wed, 28 Oct 2020 00:46:54 GMT  
		Size: 22.5 MB (22458898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70377bd3b7462785e5ffc2ed4d37625d05a77c4a2cb81512a3384a4a54bd2b1c`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 2.3 MB (2344977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c0bc3a37c84a0326222e1b09a3d44501dd3c4eda61273636651cf13eba57`  
		Last Modified: Wed, 28 Oct 2020 00:46:46 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1fb91b247cfc17bc416453741557544c0e431a6523166d277138d77dbfec99`  
		Last Modified: Wed, 28 Oct 2020 01:22:18 GMT  
		Size: 10.4 MB (10371039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92a8910d01ece7b23e329955fe0dcaa4fb25bf2d455fcc19ee9f459bcdce60`  
		Last Modified: Wed, 28 Oct 2020 01:22:13 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:2fa83656140da9d0fefcb7f94d5cc01679aa51537393c39b894b864cfd289ad7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38164799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f28a4f302c5fbdf42c0e2f1d15982b8fe2ab17ca00c8b660bc83f8ba5cb4563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:43:52 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:51:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:51:50 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:51:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:51:57 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:51:58 GMT
CMD ["node"]
# Thu, 17 Dec 2020 10:58:01 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 10:58:02 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 10:58:31 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 10:58:33 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 10:58:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 10:58:35 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 10:58:36 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 10:58:36 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 10:58:37 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 10:58:38 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 10:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 10:58:39 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc51f76858a2bdf99f2ca046c78849a1bc026e7277fad7b33ac8407b059a83`  
		Last Modified: Thu, 17 Dec 2020 03:59:31 GMT  
		Size: 22.7 MB (22714569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c9a78c1ec5f48a56201a42f2108b8f8a83cfa3d76e3865f8a0589b14171db3`  
		Last Modified: Thu, 17 Dec 2020 03:59:23 GMT  
		Size: 2.4 MB (2403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad951e768db1398a1e9d1a94bb1bdadcd55b20dbbab5e773522168c8503ba34`  
		Last Modified: Thu, 17 Dec 2020 03:59:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89002435d956e1557f411c11a562fc6b670582cf612b287df625af860e33ae62`  
		Last Modified: Thu, 17 Dec 2020 10:59:03 GMT  
		Size: 10.3 MB (10320650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b68f55df2a970e57dc6a00cfae05a1f7a833eb867a5381e4d92fb9a440cfcf8`  
		Last Modified: Thu, 17 Dec 2020 10:58:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; 386

```console
$ docker pull express-gateway@sha256:c9cb6e38a97c7ff7cc6199588a0f906dee1ba85ea94c04d1facbe4759fb3649f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8fef8170b13e6567e1edc0f8bb097b8d0c4601b6c19b6de1f1d8d4af38642d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:39 GMT
ADD file:c8f5b26cfa9b90dfe6ca805f2101bd199c87b93faed2af74df0cbe54ea28fa6d in / 
# Thu, 17 Dec 2020 00:38:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:02:10 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 03:31:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 03:31:17 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 03:31:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 03:31:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 03:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 03:31:21 GMT
CMD ["node"]
# Thu, 17 Dec 2020 08:48:23 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 08:48:23 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 08:48:49 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 08:48:49 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 08:48:50 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 08:48:50 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 08:48:50 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 08:48:50 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 08:48:50 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 08:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 08:48:51 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:60519712d04c07db59906a2e14fa87c037b6504d612ba116ea1ef94ae08a650b`  
		Last Modified: Thu, 17 Dec 2020 00:39:32 GMT  
		Size: 2.8 MB (2810512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f36a347448a466b18b94dc3e95cab6f5e09ebf07a01ce0f700b38313e503797`  
		Last Modified: Thu, 17 Dec 2020 03:32:12 GMT  
		Size: 22.7 MB (22691122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164d2c5829f7da75702be63355d41c7f3436defede5620d02ad36ca9ae9f847e`  
		Last Modified: Thu, 17 Dec 2020 03:32:06 GMT  
		Size: 2.4 MB (2364286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1609a84c1b04bf2fd9f8e56c5ac7d8a8773173bf6c24946c64a32aa8ebc68b25`  
		Last Modified: Thu, 17 Dec 2020 03:32:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fb2291d38d36981d4ae67e7f4019a7ace5a88d55ed6c89e400456e4167d82f`  
		Last Modified: Thu, 17 Dec 2020 08:49:08 GMT  
		Size: 10.3 MB (10321292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ae5bbc372d044bacfadc24bb46022e8f8b66a61a43ad5461393fb0176640ef`  
		Last Modified: Thu, 17 Dec 2020 08:49:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:607107e5af6a25e07e97e9c5e28daf5944b2363f12289e66e5d62ff2df3d00a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40037900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f989a954bc276a8c09aa56f1dc9c7661cb7c07544212bea8c41db2331462a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 02:02:01 GMT
ENV NODE_VERSION=10.23.0
# Wed, 28 Oct 2020 02:17:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 28 Oct 2020 02:17:38 GMT
ENV YARN_VERSION=1.22.5
# Wed, 28 Oct 2020 02:18:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 28 Oct 2020 02:18:01 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 28 Oct 2020 02:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 02:18:10 GMT
CMD ["node"]
# Wed, 28 Oct 2020 03:22:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 28 Oct 2020 03:22:17 GMT
ARG EG_VERSION=1.16.10
# Wed, 28 Oct 2020 03:22:53 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 28 Oct 2020 03:22:58 GMT
ENV NODE_ENV=production
# Wed, 28 Oct 2020 03:23:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 28 Oct 2020 03:23:07 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 28 Oct 2020 03:23:11 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 28 Oct 2020 03:23:14 GMT
VOLUME [/var/lib/eg]
# Wed, 28 Oct 2020 03:23:17 GMT
EXPOSE 8080 9876
# Wed, 28 Oct 2020 03:23:19 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 28 Oct 2020 03:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Oct 2020 03:23:27 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cf90450daa2d6b1b9cef450ab59c5cd7e844ee5787a4445eb8219e6554ad9c`  
		Last Modified: Wed, 28 Oct 2020 02:44:46 GMT  
		Size: 24.4 MB (24441894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401705d0a055c4c81009152ac255870e16555753cfa8b93e36cc1664d7eb478b`  
		Last Modified: Wed, 28 Oct 2020 02:44:41 GMT  
		Size: 2.4 MB (2403283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd907dddb2a9087a416892896a286c062b3edb82535a7c57d68ed458fa33b`  
		Last Modified: Wed, 28 Oct 2020 02:44:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a627da8d61d27e5bfd4ed08709dcf284498d3558dc59d58749c5658233bde9d8`  
		Last Modified: Wed, 28 Oct 2020 03:23:48 GMT  
		Size: 10.4 MB (10370098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0e0f877eb276a3f2daa2e390f668f6c9f32889b91b707664519d122858c34`  
		Last Modified: Wed, 28 Oct 2020 03:23:45 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; s390x

```console
$ docker pull express-gateway@sha256:b4f436da198547000c6943edbf71fbe6ccbe537ed4bc57594e43f21f69466498
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37818086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1163f758cb0b7723fa4c1c145e5043c73b54469aa054f704832cf46f7923370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:44 GMT
ADD file:9e0a7f4c5f520dabbf66a5d4312ceeb614fc5073fca7a248eb070cd99f4b75ff in / 
# Wed, 16 Dec 2020 23:41:44 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 05:26:06 GMT
ENV NODE_VERSION=10.23.0
# Thu, 17 Dec 2020 05:46:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="149ab80ab7e618acd7b8402dbb86ff13d89cd4a0b39d45ee9b735944e1b89737"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       1C050899334244A8AF75E53792EF661D867B9DFA       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 17 Dec 2020 05:46:09 GMT
ENV YARN_VERSION=1.22.5
# Thu, 17 Dec 2020 05:46:13 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 17 Dec 2020 05:46:15 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 17 Dec 2020 05:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 05:46:16 GMT
CMD ["node"]
# Thu, 17 Dec 2020 11:57:17 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 17 Dec 2020 11:57:18 GMT
ARG EG_VERSION=1.16.10
# Thu, 17 Dec 2020 11:57:56 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 17 Dec 2020 11:58:02 GMT
ENV NODE_ENV=production
# Thu, 17 Dec 2020 11:58:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 17 Dec 2020 11:58:03 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 17 Dec 2020 11:58:04 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 17 Dec 2020 11:58:04 GMT
VOLUME [/var/lib/eg]
# Thu, 17 Dec 2020 11:58:05 GMT
EXPOSE 8080 9876
# Thu, 17 Dec 2020 11:58:05 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 17 Dec 2020 11:58:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 11:58:07 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:ae4c90d25da4580c1cd02a35a672d9113b17e063183b4148c463df4d33079192`  
		Last Modified: Wed, 16 Dec 2020 23:42:26 GMT  
		Size: 2.6 MB (2583287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22088d51a74c158f69cd817ecf9d4277da8bbf03cd3a1f6e4750bfa1895d2761`  
		Last Modified: Thu, 17 Dec 2020 05:50:56 GMT  
		Size: 22.5 MB (22512516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efadf5471afbfdd473e2f6e15ad368d4c74abf4ab424836ca8cc2ce4330a98c`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 2.4 MB (2400163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d69e94aa00bb65f0ad917a08bf596ae7f8361f7c360e34cd98fa90ed419083`  
		Last Modified: Thu, 17 Dec 2020 05:50:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f270cb5c8c3d0cdadf24f76514671b1ce674d550cf9d61be869bbb6e4eacb`  
		Last Modified: Thu, 17 Dec 2020 11:58:22 GMT  
		Size: 10.3 MB (10321344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee80b5bfd57041b4d925714bdec268eb008a9db6edc49c14709336600df8a0c5`  
		Last Modified: Thu, 17 Dec 2020 11:58:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

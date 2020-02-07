## `express-gateway:latest`

```console
$ docker pull express-gateway@sha256:a1bf18d2b7534cf47dee6c096cfab9e5119c0e9a5864223771ad32ab6eeaf506
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
$ docker pull express-gateway@sha256:6b6f5f22cdfe771bcd448a3d1944dd498c7e359ebc85ac80ed5669d23bb24e08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35809280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81774ef18bbf6708dd078217450a42a10d65cc4a15556126b064f497a97b2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 23:31:11 GMT
ENV NODE_VERSION=10.19.0
# Thu, 06 Feb 2020 23:31:21 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="7d607297a0dd0b78861b4807733424ae288968d8653be644bedde123ddb0d96f"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Thu, 06 Feb 2020 23:31:22 GMT
ENV YARN_VERSION=1.21.1
# Thu, 06 Feb 2020 23:31:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Thu, 06 Feb 2020 23:31:26 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 06 Feb 2020 23:31:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2020 23:31:27 GMT
CMD ["node"]
# Thu, 06 Feb 2020 23:59:08 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Thu, 06 Feb 2020 23:59:08 GMT
ARG EG_VERSION=1.16.10
# Thu, 06 Feb 2020 23:59:44 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Thu, 06 Feb 2020 23:59:45 GMT
ENV NODE_ENV=production
# Thu, 06 Feb 2020 23:59:46 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Thu, 06 Feb 2020 23:59:46 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Thu, 06 Feb 2020 23:59:46 GMT
ENV CHOKIDAR_USEPOLLING=true
# Thu, 06 Feb 2020 23:59:47 GMT
VOLUME [/var/lib/eg]
# Thu, 06 Feb 2020 23:59:47 GMT
EXPOSE 8080 9876
# Thu, 06 Feb 2020 23:59:48 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Thu, 06 Feb 2020 23:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2020 23:59:48 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0188bce71676084445ab177ba0d256ffebbbc85516154b44fd4375d1742a8ed7`  
		Last Modified: Thu, 06 Feb 2020 23:42:14 GMT  
		Size: 22.5 MB (22526185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62af20101b79aebcd3136b39c8c31ed095e89be6def3030b9e4fa388447be81`  
		Last Modified: Thu, 06 Feb 2020 23:42:06 GMT  
		Size: 1.3 MB (1264633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bffdb76255cd583bb9c6d95be9f9e6bab4fe3820b2d039ab8ca942400b712be`  
		Last Modified: Thu, 06 Feb 2020 23:42:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6cfd2088e749216d67e6cc35c10f50b7e605c41970aa0edca6b71913f9442a`  
		Last Modified: Fri, 07 Feb 2020 00:00:08 GMT  
		Size: 9.2 MB (9214724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7005b85ec79f6c2cf5cd75e0dadd5b4ec90fbeb1ae0b72699b2dfa5d1352e5a2`  
		Last Modified: Thu, 06 Feb 2020 23:59:59 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:e891782fc6556a5c2730b05e2236ae2351070afadf84d405185c0b33823018d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36082206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6b4f68e6232c9970a6ac33aeee47a39b0300602ff68667a346bb8a6392c032`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2020 00:22:06 GMT
ENV NODE_VERSION=10.19.0
# Fri, 07 Feb 2020 00:28:57 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="7d607297a0dd0b78861b4807733424ae288968d8653be644bedde123ddb0d96f"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 07 Feb 2020 00:29:00 GMT
ENV YARN_VERSION=1.21.1
# Fri, 07 Feb 2020 00:29:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 07 Feb 2020 00:29:07 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 07 Feb 2020 00:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 00:29:09 GMT
CMD ["node"]
# Fri, 07 Feb 2020 01:34:11 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Fri, 07 Feb 2020 01:34:12 GMT
ARG EG_VERSION=1.16.10
# Fri, 07 Feb 2020 01:34:44 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Fri, 07 Feb 2020 01:34:46 GMT
ENV NODE_ENV=production
# Fri, 07 Feb 2020 01:34:46 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Fri, 07 Feb 2020 01:34:47 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Fri, 07 Feb 2020 01:34:47 GMT
ENV CHOKIDAR_USEPOLLING=true
# Fri, 07 Feb 2020 01:34:48 GMT
VOLUME [/var/lib/eg]
# Fri, 07 Feb 2020 01:34:48 GMT
EXPOSE 8080 9876
# Fri, 07 Feb 2020 01:34:49 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:34:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 01:34:50 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c1d8c92cca709608f26877cfee4d6d828c5d73b991f46e4d9ea0acf95e89b`  
		Last Modified: Fri, 07 Feb 2020 00:40:20 GMT  
		Size: 22.8 MB (22815511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6643721447bab519193b49460faafbecfb75accb5d49a96feb816d6a5f81a`  
		Last Modified: Fri, 07 Feb 2020 00:40:13 GMT  
		Size: 1.3 MB (1327771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01663b53d45e3913338ed0b443697f0c9a56b6046a26539280e749f379ed8c33`  
		Last Modified: Fri, 07 Feb 2020 00:40:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dac4c6564d3fc0982f507652b18b79a81c360083a44e367267bd4bd3e2f733`  
		Last Modified: Fri, 07 Feb 2020 01:35:13 GMT  
		Size: 9.2 MB (9215069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b47874f5eef5c8d89d1bce549c136a6882a9d3446503d0fdb0eff28b8600b38`  
		Last Modified: Fri, 07 Feb 2020 01:35:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; 386

```console
$ docker pull express-gateway@sha256:a53459262ec6d94e0631ddc607f609c811d4b76afd33ae9d379f4db7b4caab5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36089051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5aaf24fdbf0e823bb2660c1ba4da22d59c1216c686079c8c45e2e93359d1ca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2020 02:52:33 GMT
ENV NODE_VERSION=10.19.0
# Fri, 07 Feb 2020 03:22:19 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="7d607297a0dd0b78861b4807733424ae288968d8653be644bedde123ddb0d96f"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 07 Feb 2020 03:22:19 GMT
ENV YARN_VERSION=1.21.1
# Fri, 07 Feb 2020 03:22:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 07 Feb 2020 03:22:23 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 07 Feb 2020 03:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 03:22:23 GMT
CMD ["node"]
# Fri, 07 Feb 2020 04:34:12 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Fri, 07 Feb 2020 04:34:12 GMT
ARG EG_VERSION=1.16.10
# Fri, 07 Feb 2020 04:34:32 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Fri, 07 Feb 2020 04:34:33 GMT
ENV NODE_ENV=production
# Fri, 07 Feb 2020 04:34:33 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Fri, 07 Feb 2020 04:34:33 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Fri, 07 Feb 2020 04:34:33 GMT
ENV CHOKIDAR_USEPOLLING=true
# Fri, 07 Feb 2020 04:34:34 GMT
VOLUME [/var/lib/eg]
# Fri, 07 Feb 2020 04:34:34 GMT
EXPOSE 8080 9876
# Fri, 07 Feb 2020 04:34:34 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Fri, 07 Feb 2020 04:34:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 04:34:34 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a6bb214a902330e66bec77e86125717c84c2dd01e8f63fecc7ae16e684a6e2`  
		Last Modified: Fri, 07 Feb 2020 03:24:29 GMT  
		Size: 22.8 MB (22779984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c01e29501c48fae9975dfffffd55b2e7bc0e01862ac8166303930259f9b1ff`  
		Last Modified: Fri, 07 Feb 2020 03:24:23 GMT  
		Size: 1.3 MB (1327761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a6340b0be8bfbebc4b05f612ab0a661f8e2ec5e8fc9b376e9bb575e30f378a`  
		Last Modified: Fri, 07 Feb 2020 03:24:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad30a9d5914ef630363ae2bf8f5161e63d5197d5bec9c572735987e598ecf76`  
		Last Modified: Fri, 07 Feb 2020 04:34:50 GMT  
		Size: 9.2 MB (9173970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be98bd78a52a01fb34e72324c99dbe0d610be1673fbcaa610e2b7d4a4d90dcf0`  
		Last Modified: Fri, 07 Feb 2020 04:34:43 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:233cace8209675d78db3b9f5c907b54657a4657cd3cf04f2acac14bb05560ac5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37900740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a8ba6cbb7bf9b6bb12b542ae26e5b502f1b95cc056f0c72101088ff053eae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2020 00:53:07 GMT
ENV NODE_VERSION=10.19.0
# Fri, 07 Feb 2020 01:05:10 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="7d607297a0dd0b78861b4807733424ae288968d8653be644bedde123ddb0d96f"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 07 Feb 2020 01:05:13 GMT
ENV YARN_VERSION=1.21.1
# Fri, 07 Feb 2020 01:05:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 07 Feb 2020 01:05:21 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 01:05:25 GMT
CMD ["node"]
# Fri, 07 Feb 2020 02:18:10 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Fri, 07 Feb 2020 02:18:15 GMT
ARG EG_VERSION=1.16.10
# Fri, 07 Feb 2020 02:18:43 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Fri, 07 Feb 2020 02:18:50 GMT
ENV NODE_ENV=production
# Fri, 07 Feb 2020 02:18:53 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Fri, 07 Feb 2020 02:18:54 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Fri, 07 Feb 2020 02:18:56 GMT
ENV CHOKIDAR_USEPOLLING=true
# Fri, 07 Feb 2020 02:18:58 GMT
VOLUME [/var/lib/eg]
# Fri, 07 Feb 2020 02:19:00 GMT
EXPOSE 8080 9876
# Fri, 07 Feb 2020 02:19:01 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Fri, 07 Feb 2020 02:19:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 02:19:05 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a52459c5b4a4667b7208e39ee1ec8c5006613ff2f23300c9d8f73b80e66011c`  
		Last Modified: Fri, 07 Feb 2020 01:19:57 GMT  
		Size: 24.5 MB (24535285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b2ae12b8d35cb886547e2830e7fdbe1910b34b3fe93b18fb9ca6d22e3131a4`  
		Last Modified: Fri, 07 Feb 2020 01:19:23 GMT  
		Size: 1.3 MB (1327828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b4af98c4a84012ba8deea9d67ab94c9e280e3237a384cf6e66fa53d7a6ddcc`  
		Last Modified: Fri, 07 Feb 2020 01:19:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bc47b1b093a320939c133d767fe65b3675079d19484a81039d0a9245f2ab76`  
		Last Modified: Fri, 07 Feb 2020 02:19:34 GMT  
		Size: 9.2 MB (9214726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9eb6b2ff0561599718c0f0b305c4b1d1f4562a27400fc6f881f76effbfe385`  
		Last Modified: Fri, 07 Feb 2020 02:19:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; s390x

```console
$ docker pull express-gateway@sha256:398b2c3c889c0277c248a3b8549a829df3878f017e7ee03a1bc077d8611fc2e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35720390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d30b2b5b978fecb3c95793a9dc633ca961dd4091e582335d21bc237219eca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2020 00:39:08 GMT
ENV NODE_VERSION=10.19.0
# Fri, 07 Feb 2020 00:51:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="7d607297a0dd0b78861b4807733424ae288968d8653be644bedde123ddb0d96f"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 07 Feb 2020 00:51:12 GMT
ENV YARN_VERSION=1.21.1
# Fri, 07 Feb 2020 00:51:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 07 Feb 2020 00:51:15 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 07 Feb 2020 00:51:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 00:51:16 GMT
CMD ["node"]
# Fri, 07 Feb 2020 01:41:49 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Fri, 07 Feb 2020 01:41:49 GMT
ARG EG_VERSION=1.16.10
# Fri, 07 Feb 2020 01:42:01 GMT
# ARGS: EG_VERSION=1.16.10
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Fri, 07 Feb 2020 01:42:03 GMT
ENV NODE_ENV=production
# Fri, 07 Feb 2020 01:42:03 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Fri, 07 Feb 2020 01:42:03 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Fri, 07 Feb 2020 01:42:03 GMT
ENV CHOKIDAR_USEPOLLING=true
# Fri, 07 Feb 2020 01:42:04 GMT
VOLUME [/var/lib/eg]
# Fri, 07 Feb 2020 01:42:04 GMT
EXPOSE 8080 9876
# Fri, 07 Feb 2020 01:42:04 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:42:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 01:42:04 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d69bfd27db618b54f5d2a6a07ba36dae97488abe554566eda789fd7205bfcf`  
		Last Modified: Fri, 07 Feb 2020 00:57:51 GMT  
		Size: 22.6 MB (22601155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3acf30eeed702472ffaa8999e4a996bc075ca3563953b45841bb9141b34c9d`  
		Last Modified: Fri, 07 Feb 2020 00:57:51 GMT  
		Size: 1.3 MB (1327781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c0ffc5c96f60381bec6bb097419d02e940ebcef1559d67682dec8e31f4fbfa`  
		Last Modified: Fri, 07 Feb 2020 00:58:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b46d6548862abb1e21d4837224c3007e9066acfbe9258365142d2ff6d144645`  
		Last Modified: Fri, 07 Feb 2020 01:42:18 GMT  
		Size: 9.2 MB (9208650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636c34f4e42cc4cd13630e514984ee06372df18aa0e15297a0f19e7c00912982`  
		Last Modified: Fri, 07 Feb 2020 01:42:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

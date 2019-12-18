## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:d244067c4c89ec96b6b52c85ab8cefe4e8e4c5ef3cf0c36a7c19737297eef8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:76d3fb1546529555270724f840b2887a9b7f13ca2685edbf483165d0f1168a47
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38324826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365cb038f2dba7e5a8065ca3d753dcc2d7a1347c60c1975c745fab4e522af8b2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2019 16:24:13 GMT
ENV NODE_VERSION=8.17.0
# Wed, 18 Dec 2019 16:24:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bd085bf3bf9d442500f78943e7f04631c7eaa888a3bf42c1f40bea74c3d1d6f8"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 18 Dec 2019 16:24:18 GMT
ENV YARN_VERSION=1.21.1
# Wed, 18 Dec 2019 16:24:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 18 Dec 2019 16:24:21 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 18 Dec 2019 16:24:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2019 16:24:21 GMT
CMD ["node"]
# Wed, 18 Dec 2019 16:54:45 GMT
RUN apk add --no-cache bash tini
# Wed, 18 Dec 2019 16:54:46 GMT
EXPOSE 8081
# Wed, 18 Dec 2019 16:54:46 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 18 Dec 2019 16:54:46 GMT
ENV MONGO_EXPRESS=0.49.0
# Wed, 18 Dec 2019 16:55:07 GMT
RUN npm install mongo-express@$MONGO_EXPRESS
# Wed, 18 Dec 2019 16:55:08 GMT
COPY file:58292318f4d4eebb73af5f654a480f4db1e1bb8a29365676b6ccf54504b61984 in / 
# Wed, 18 Dec 2019 16:55:08 GMT
WORKDIR /node_modules/mongo-express
# Wed, 18 Dec 2019 16:55:10 GMT
RUN cp config.default.js config.js
# Wed, 18 Dec 2019 16:55:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 18 Dec 2019 16:55:10 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc80e86c6d190022159c38f627e2ee6be180600859ce621210f303a10b9c232`  
		Last Modified: Wed, 18 Dec 2019 16:34:34 GMT  
		Size: 20.2 MB (20160544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10ee41aaa59aba925a5a1cdeb9ec2b496668e7fbb146b0ac470090245fec350`  
		Last Modified: Wed, 18 Dec 2019 16:34:30 GMT  
		Size: 1.3 MB (1263988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50008be078a9e55600e0b526c7c42644560f41d626c8821a87821d58f8e188d8`  
		Last Modified: Wed, 18 Dec 2019 16:34:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a73774c47b74df9f85589d49b907a58c0add40b981d1c8f82ade00a8715ea`  
		Last Modified: Wed, 18 Dec 2019 16:55:22 GMT  
		Size: 1.2 MB (1221342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a32d8476ee1ad5b2c891603d6e5e26526300d351dc286106cc0113b87ca7d`  
		Last Modified: Wed, 18 Dec 2019 16:55:25 GMT  
		Size: 12.9 MB (12888202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1033c0fac633e3d8616fccd761ffb6408fc7764740ee06b5b19dc37ff8edb99b`  
		Last Modified: Wed, 18 Dec 2019 16:55:21 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b841f73bc8448ad0cae027eeb28489ea37fd489e9a9d718d8a1254fb584fcd`  
		Last Modified: Wed, 18 Dec 2019 16:55:21 GMT  
		Size: 2.8 KB (2763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7764dba350d78a8a8583e5b06e62c51b04294482742d4f4bd3542d669e890cd9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38319719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ebc1803cad18806a26492526c6f6857639bee5774ec6789b2d1e72225ca4ee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2019 16:47:38 GMT
ENV NODE_VERSION=8.17.0
# Wed, 18 Dec 2019 16:52:36 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bd085bf3bf9d442500f78943e7f04631c7eaa888a3bf42c1f40bea74c3d1d6f8"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 18 Dec 2019 16:52:46 GMT
ENV YARN_VERSION=1.21.1
# Wed, 18 Dec 2019 16:53:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 18 Dec 2019 16:53:02 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 18 Dec 2019 16:53:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2019 16:53:04 GMT
CMD ["node"]
# Wed, 18 Dec 2019 18:18:58 GMT
RUN apk add --no-cache bash tini
# Wed, 18 Dec 2019 18:18:58 GMT
EXPOSE 8081
# Wed, 18 Dec 2019 18:18:59 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 18 Dec 2019 18:18:59 GMT
ENV MONGO_EXPRESS=0.49.0
# Wed, 18 Dec 2019 18:19:19 GMT
RUN npm install mongo-express@$MONGO_EXPRESS
# Wed, 18 Dec 2019 18:19:21 GMT
COPY file:58292318f4d4eebb73af5f654a480f4db1e1bb8a29365676b6ccf54504b61984 in / 
# Wed, 18 Dec 2019 18:19:21 GMT
WORKDIR /node_modules/mongo-express
# Wed, 18 Dec 2019 18:19:23 GMT
RUN cp config.default.js config.js
# Wed, 18 Dec 2019 18:19:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 18 Dec 2019 18:19:24 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d8e66c490872cc8b62a5f7d1040eb197d9a165ac131d89a55d152ccd5fd5a5`  
		Last Modified: Wed, 18 Dec 2019 17:55:22 GMT  
		Size: 20.1 MB (20149048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673584b01ec75163d35ef6d4784147cce2ad188a437fa58a827b6837b200027`  
		Last Modified: Wed, 18 Dec 2019 17:55:14 GMT  
		Size: 1.3 MB (1327118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b016e519d7de4b3f50416cff87db55186e7be5e89dfa1128c3339b1025161580`  
		Last Modified: Wed, 18 Dec 2019 17:55:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba72fb84ea26f2d9262b695d4c7d4414668cc451ade793e126281cf55c2f4a60`  
		Last Modified: Wed, 18 Dec 2019 18:19:34 GMT  
		Size: 1.2 MB (1234265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed802b65d724169ae440f19cb57367fc9cd49aeb3bda149625dba2908a3df344`  
		Last Modified: Wed, 18 Dec 2019 18:19:38 GMT  
		Size: 12.9 MB (12887895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667554c5190d6e8d8d45c309398c8c51c8b0011d214bae07f7919c10efcc7c6c`  
		Last Modified: Wed, 18 Dec 2019 18:19:34 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62431c1e16ba6d7f7e16f98788efe355062f1f0426c9e618e6c0e2a0217e248f`  
		Last Modified: Wed, 18 Dec 2019 18:19:33 GMT  
		Size: 2.8 KB (2763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

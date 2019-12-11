<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:2`](#rocketchat2)
-	[`rocket.chat:2.3`](#rocketchat23)
-	[`rocket.chat:2.3.1`](#rocketchat231)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:2`

```console
$ docker pull rocket.chat@sha256:71a2117de79cea1c64f8f6ec565a25f4937bbc6769d100c9f967b33be5486b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a7ad251ead7d03de0f836d083911c97c17a253abd30615c87ba68176d561d757
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201669610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497b36a9e0f86576c9b41f9c383cc42871877a4ebacfdb095ad7047bae186741`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 22 Nov 2019 14:56:04 GMT
ADD file:41e78f98c436ed4f05c337e67e10439bb860bbea86c78368cc0e80100026cf40 in / 
# Fri, 22 Nov 2019 14:56:04 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:52:52 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD8F2338BAE7501E3DD5AC78C273792F7D83545D
# Sat, 23 Nov 2019 00:52:52 GMT
ENV NODE_VERSION=8.15.1
# Sat, 23 Nov 2019 00:52:53 GMT
ENV NODE_ENV=production
# Tue, 10 Dec 2019 22:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates curl fontconfig; 	rm -rf /var/lib/apt/lists/*; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz"; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"; 	gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc; 	grep " node-v$NODE_VERSION-linux-x64.tar.gz\$" SHASUMS256.txt | sha256sum -c -; 	tar -xf "node-v$NODE_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1 --no-same-owner; 	rm "node-v$NODE_VERSION-linux-x64.tar.gz" SHASUMS256.txt.asc SHASUMS256.txt; 	npm cache clear --force
# Tue, 10 Dec 2019 22:28:01 GMT
LABEL maintainer=buildmaster@rocket.chat
# Tue, 10 Dec 2019 22:28:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 10 Dec 2019 22:28:03 GMT
VOLUME [/app/uploads]
# Tue, 10 Dec 2019 22:28:04 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Tue, 10 Dec 2019 22:28:04 GMT
ENV RC_VERSION=2.3.1
# Tue, 10 Dec 2019 22:28:05 GMT
WORKDIR /app
# Tue, 10 Dec 2019 22:29:10 GMT
RUN curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 10 Dec 2019 22:29:13 GMT
USER rocketchat
# Tue, 10 Dec 2019 22:29:13 GMT
WORKDIR /app/bundle
# Tue, 10 Dec 2019 22:29:13 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 10 Dec 2019 22:29:14 GMT
EXPOSE 3000
# Tue, 10 Dec 2019 22:29:14 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:02d147d362835efa14b8a83e3b4a7dd20dd53dd0ba1619316a691acb9e614c13`  
		Last Modified: Fri, 22 Nov 2019 15:03:20 GMT  
		Size: 30.2 MB (30159468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3449a347fc04f19e863b2862c950110099dc301f5b603e215520c43f26c4478e`  
		Last Modified: Sat, 23 Nov 2019 00:55:52 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef55fb9cfd0b5be9a6229a9c800cd4f8283cdf0d57dbfcb400289073807e2b`  
		Last Modified: Tue, 10 Dec 2019 22:29:45 GMT  
		Size: 24.9 MB (24911372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bd6158679c2c1363d71942af8651c8dfb114f5651ab127f410c81b021c7db0`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f627698addc3a094c9fd397c52fcf5359c01ed3a49fccaf53603df3de73e`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 14.7 KB (14662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3d8900e7e5c868f6e724250a5f13a6fcbf5e35a41acd1f928a0392cd1820ec`  
		Last Modified: Tue, 10 Dec 2019 22:30:26 GMT  
		Size: 146.6 MB (146572161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:2.3`

```console
$ docker pull rocket.chat@sha256:71a2117de79cea1c64f8f6ec565a25f4937bbc6769d100c9f967b33be5486b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:2.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a7ad251ead7d03de0f836d083911c97c17a253abd30615c87ba68176d561d757
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201669610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497b36a9e0f86576c9b41f9c383cc42871877a4ebacfdb095ad7047bae186741`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 22 Nov 2019 14:56:04 GMT
ADD file:41e78f98c436ed4f05c337e67e10439bb860bbea86c78368cc0e80100026cf40 in / 
# Fri, 22 Nov 2019 14:56:04 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:52:52 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD8F2338BAE7501E3DD5AC78C273792F7D83545D
# Sat, 23 Nov 2019 00:52:52 GMT
ENV NODE_VERSION=8.15.1
# Sat, 23 Nov 2019 00:52:53 GMT
ENV NODE_ENV=production
# Tue, 10 Dec 2019 22:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates curl fontconfig; 	rm -rf /var/lib/apt/lists/*; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz"; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"; 	gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc; 	grep " node-v$NODE_VERSION-linux-x64.tar.gz\$" SHASUMS256.txt | sha256sum -c -; 	tar -xf "node-v$NODE_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1 --no-same-owner; 	rm "node-v$NODE_VERSION-linux-x64.tar.gz" SHASUMS256.txt.asc SHASUMS256.txt; 	npm cache clear --force
# Tue, 10 Dec 2019 22:28:01 GMT
LABEL maintainer=buildmaster@rocket.chat
# Tue, 10 Dec 2019 22:28:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 10 Dec 2019 22:28:03 GMT
VOLUME [/app/uploads]
# Tue, 10 Dec 2019 22:28:04 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Tue, 10 Dec 2019 22:28:04 GMT
ENV RC_VERSION=2.3.1
# Tue, 10 Dec 2019 22:28:05 GMT
WORKDIR /app
# Tue, 10 Dec 2019 22:29:10 GMT
RUN curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 10 Dec 2019 22:29:13 GMT
USER rocketchat
# Tue, 10 Dec 2019 22:29:13 GMT
WORKDIR /app/bundle
# Tue, 10 Dec 2019 22:29:13 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 10 Dec 2019 22:29:14 GMT
EXPOSE 3000
# Tue, 10 Dec 2019 22:29:14 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:02d147d362835efa14b8a83e3b4a7dd20dd53dd0ba1619316a691acb9e614c13`  
		Last Modified: Fri, 22 Nov 2019 15:03:20 GMT  
		Size: 30.2 MB (30159468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3449a347fc04f19e863b2862c950110099dc301f5b603e215520c43f26c4478e`  
		Last Modified: Sat, 23 Nov 2019 00:55:52 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef55fb9cfd0b5be9a6229a9c800cd4f8283cdf0d57dbfcb400289073807e2b`  
		Last Modified: Tue, 10 Dec 2019 22:29:45 GMT  
		Size: 24.9 MB (24911372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bd6158679c2c1363d71942af8651c8dfb114f5651ab127f410c81b021c7db0`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f627698addc3a094c9fd397c52fcf5359c01ed3a49fccaf53603df3de73e`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 14.7 KB (14662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3d8900e7e5c868f6e724250a5f13a6fcbf5e35a41acd1f928a0392cd1820ec`  
		Last Modified: Tue, 10 Dec 2019 22:30:26 GMT  
		Size: 146.6 MB (146572161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:2.3.1`

```console
$ docker pull rocket.chat@sha256:71a2117de79cea1c64f8f6ec565a25f4937bbc6769d100c9f967b33be5486b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:2.3.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a7ad251ead7d03de0f836d083911c97c17a253abd30615c87ba68176d561d757
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201669610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497b36a9e0f86576c9b41f9c383cc42871877a4ebacfdb095ad7047bae186741`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 22 Nov 2019 14:56:04 GMT
ADD file:41e78f98c436ed4f05c337e67e10439bb860bbea86c78368cc0e80100026cf40 in / 
# Fri, 22 Nov 2019 14:56:04 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:52:52 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD8F2338BAE7501E3DD5AC78C273792F7D83545D
# Sat, 23 Nov 2019 00:52:52 GMT
ENV NODE_VERSION=8.15.1
# Sat, 23 Nov 2019 00:52:53 GMT
ENV NODE_ENV=production
# Tue, 10 Dec 2019 22:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates curl fontconfig; 	rm -rf /var/lib/apt/lists/*; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz"; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"; 	gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc; 	grep " node-v$NODE_VERSION-linux-x64.tar.gz\$" SHASUMS256.txt | sha256sum -c -; 	tar -xf "node-v$NODE_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1 --no-same-owner; 	rm "node-v$NODE_VERSION-linux-x64.tar.gz" SHASUMS256.txt.asc SHASUMS256.txt; 	npm cache clear --force
# Tue, 10 Dec 2019 22:28:01 GMT
LABEL maintainer=buildmaster@rocket.chat
# Tue, 10 Dec 2019 22:28:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 10 Dec 2019 22:28:03 GMT
VOLUME [/app/uploads]
# Tue, 10 Dec 2019 22:28:04 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Tue, 10 Dec 2019 22:28:04 GMT
ENV RC_VERSION=2.3.1
# Tue, 10 Dec 2019 22:28:05 GMT
WORKDIR /app
# Tue, 10 Dec 2019 22:29:10 GMT
RUN curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 10 Dec 2019 22:29:13 GMT
USER rocketchat
# Tue, 10 Dec 2019 22:29:13 GMT
WORKDIR /app/bundle
# Tue, 10 Dec 2019 22:29:13 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 10 Dec 2019 22:29:14 GMT
EXPOSE 3000
# Tue, 10 Dec 2019 22:29:14 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:02d147d362835efa14b8a83e3b4a7dd20dd53dd0ba1619316a691acb9e614c13`  
		Last Modified: Fri, 22 Nov 2019 15:03:20 GMT  
		Size: 30.2 MB (30159468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3449a347fc04f19e863b2862c950110099dc301f5b603e215520c43f26c4478e`  
		Last Modified: Sat, 23 Nov 2019 00:55:52 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef55fb9cfd0b5be9a6229a9c800cd4f8283cdf0d57dbfcb400289073807e2b`  
		Last Modified: Tue, 10 Dec 2019 22:29:45 GMT  
		Size: 24.9 MB (24911372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bd6158679c2c1363d71942af8651c8dfb114f5651ab127f410c81b021c7db0`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f627698addc3a094c9fd397c52fcf5359c01ed3a49fccaf53603df3de73e`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 14.7 KB (14662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3d8900e7e5c868f6e724250a5f13a6fcbf5e35a41acd1f928a0392cd1820ec`  
		Last Modified: Tue, 10 Dec 2019 22:30:26 GMT  
		Size: 146.6 MB (146572161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:71a2117de79cea1c64f8f6ec565a25f4937bbc6769d100c9f967b33be5486b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a7ad251ead7d03de0f836d083911c97c17a253abd30615c87ba68176d561d757
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201669610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497b36a9e0f86576c9b41f9c383cc42871877a4ebacfdb095ad7047bae186741`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 22 Nov 2019 14:56:04 GMT
ADD file:41e78f98c436ed4f05c337e67e10439bb860bbea86c78368cc0e80100026cf40 in / 
# Fri, 22 Nov 2019 14:56:04 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:52:52 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD8F2338BAE7501E3DD5AC78C273792F7D83545D
# Sat, 23 Nov 2019 00:52:52 GMT
ENV NODE_VERSION=8.15.1
# Sat, 23 Nov 2019 00:52:53 GMT
ENV NODE_ENV=production
# Tue, 10 Dec 2019 22:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates curl fontconfig; 	rm -rf /var/lib/apt/lists/*; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz"; 	curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"; 	gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc; 	grep " node-v$NODE_VERSION-linux-x64.tar.gz\$" SHASUMS256.txt | sha256sum -c -; 	tar -xf "node-v$NODE_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1 --no-same-owner; 	rm "node-v$NODE_VERSION-linux-x64.tar.gz" SHASUMS256.txt.asc SHASUMS256.txt; 	npm cache clear --force
# Tue, 10 Dec 2019 22:28:01 GMT
LABEL maintainer=buildmaster@rocket.chat
# Tue, 10 Dec 2019 22:28:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 10 Dec 2019 22:28:03 GMT
VOLUME [/app/uploads]
# Tue, 10 Dec 2019 22:28:04 GMT
RUN gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Tue, 10 Dec 2019 22:28:04 GMT
ENV RC_VERSION=2.3.1
# Tue, 10 Dec 2019 22:28:05 GMT
WORKDIR /app
# Tue, 10 Dec 2019 22:29:10 GMT
RUN curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 10 Dec 2019 22:29:13 GMT
USER rocketchat
# Tue, 10 Dec 2019 22:29:13 GMT
WORKDIR /app/bundle
# Tue, 10 Dec 2019 22:29:13 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 10 Dec 2019 22:29:14 GMT
EXPOSE 3000
# Tue, 10 Dec 2019 22:29:14 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:02d147d362835efa14b8a83e3b4a7dd20dd53dd0ba1619316a691acb9e614c13`  
		Last Modified: Fri, 22 Nov 2019 15:03:20 GMT  
		Size: 30.2 MB (30159468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3449a347fc04f19e863b2862c950110099dc301f5b603e215520c43f26c4478e`  
		Last Modified: Sat, 23 Nov 2019 00:55:52 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef55fb9cfd0b5be9a6229a9c800cd4f8283cdf0d57dbfcb400289073807e2b`  
		Last Modified: Tue, 10 Dec 2019 22:29:45 GMT  
		Size: 24.9 MB (24911372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bd6158679c2c1363d71942af8651c8dfb114f5651ab127f410c81b021c7db0`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f627698addc3a094c9fd397c52fcf5359c01ed3a49fccaf53603df3de73e`  
		Last Modified: Tue, 10 Dec 2019 22:29:36 GMT  
		Size: 14.7 KB (14662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3d8900e7e5c868f6e724250a5f13a6fcbf5e35a41acd1f928a0392cd1820ec`  
		Last Modified: Tue, 10 Dec 2019 22:30:26 GMT  
		Size: 146.6 MB (146572161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

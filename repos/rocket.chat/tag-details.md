<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:6`](#rocketchat6)
-	[`rocket.chat:6.10`](#rocketchat610)
-	[`rocket.chat:6.10.4`](#rocketchat6104)
-	[`rocket.chat:6.11`](#rocketchat611)
-	[`rocket.chat:6.11.1`](#rocketchat6111)
-	[`rocket.chat:6.7`](#rocketchat67)
-	[`rocket.chat:6.7.7`](#rocketchat677)
-	[`rocket.chat:6.8`](#rocketchat68)
-	[`rocket.chat:6.8.5`](#rocketchat685)
-	[`rocket.chat:6.9`](#rocketchat69)
-	[`rocket.chat:6.9.5`](#rocketchat695)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:6`

```console
$ docker pull rocket.chat@sha256:03ed9438d26b7b5e74d239c3c8fc8e072d1560066e7721f8e1f74cf01b4f1ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:5591debc687299955b91f4cb98b0fc944b7ab59157e6c235226604656adfee97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439189965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe217ee3d2de5b61cb26a77a20e7b7381139d2ab61fb67267e9705049589c0`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:28:54 GMT
ENV RC_VERSION=6.11.1
# Fri, 27 Sep 2024 05:28:54 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:30:58 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:31:07 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:31:07 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:31:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:31:08 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:31:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ea88d87cdfd8ec642e860bd03acb3b03f889fbdfc9a7daf451965ecb59b92a`  
		Last Modified: Fri, 27 Sep 2024 05:38:04 GMT  
		Size: 372.0 MB (371999325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.10`

```console
$ docker pull rocket.chat@sha256:1abbcabeedac7e454c1e06cfba6b5f5f81961a41f420cfd5e4674c41f6414366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:65c7e5c28170450f4942a8c56079bf745470cd364c67bebd33ffabb1576b6fd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.6 MB (438626275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48434542ef84a6059386cbeaaf23c24a365b9860b216296695d7873ecd301e78`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:31:18 GMT
ENV RC_VERSION=6.10.4
# Fri, 27 Sep 2024 05:31:18 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:33:29 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:33:33 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:33:33 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:33:34 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:33:34 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:33:34 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ba6b173b919f9b82ea12d88b67ed5fcf6a7e7d69fa74b97f429af6edd5de74`  
		Last Modified: Fri, 27 Sep 2024 05:39:18 GMT  
		Size: 371.4 MB (371435635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.10.4`

```console
$ docker pull rocket.chat@sha256:1abbcabeedac7e454c1e06cfba6b5f5f81961a41f420cfd5e4674c41f6414366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.10.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:65c7e5c28170450f4942a8c56079bf745470cd364c67bebd33ffabb1576b6fd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.6 MB (438626275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48434542ef84a6059386cbeaaf23c24a365b9860b216296695d7873ecd301e78`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:31:18 GMT
ENV RC_VERSION=6.10.4
# Fri, 27 Sep 2024 05:31:18 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:33:29 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:33:33 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:33:33 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:33:34 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:33:34 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:33:34 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ba6b173b919f9b82ea12d88b67ed5fcf6a7e7d69fa74b97f429af6edd5de74`  
		Last Modified: Fri, 27 Sep 2024 05:39:18 GMT  
		Size: 371.4 MB (371435635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.11`

```console
$ docker pull rocket.chat@sha256:03ed9438d26b7b5e74d239c3c8fc8e072d1560066e7721f8e1f74cf01b4f1ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.11` - linux; amd64

```console
$ docker pull rocket.chat@sha256:5591debc687299955b91f4cb98b0fc944b7ab59157e6c235226604656adfee97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439189965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe217ee3d2de5b61cb26a77a20e7b7381139d2ab61fb67267e9705049589c0`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:28:54 GMT
ENV RC_VERSION=6.11.1
# Fri, 27 Sep 2024 05:28:54 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:30:58 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:31:07 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:31:07 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:31:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:31:08 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:31:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ea88d87cdfd8ec642e860bd03acb3b03f889fbdfc9a7daf451965ecb59b92a`  
		Last Modified: Fri, 27 Sep 2024 05:38:04 GMT  
		Size: 372.0 MB (371999325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.11.1`

```console
$ docker pull rocket.chat@sha256:03ed9438d26b7b5e74d239c3c8fc8e072d1560066e7721f8e1f74cf01b4f1ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.11.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:5591debc687299955b91f4cb98b0fc944b7ab59157e6c235226604656adfee97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439189965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe217ee3d2de5b61cb26a77a20e7b7381139d2ab61fb67267e9705049589c0`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:28:54 GMT
ENV RC_VERSION=6.11.1
# Fri, 27 Sep 2024 05:28:54 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:30:58 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:31:07 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:31:07 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:31:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:31:08 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:31:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ea88d87cdfd8ec642e860bd03acb3b03f889fbdfc9a7daf451965ecb59b92a`  
		Last Modified: Fri, 27 Sep 2024 05:38:04 GMT  
		Size: 372.0 MB (371999325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.7`

```console
$ docker pull rocket.chat@sha256:e651f33a3390cbbc98eb744453fbfbd0ef42d7e451af39269a68bd343bf34957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3bc500a2ec9e09cebc1fd3f98398f58068de651a334ad0f4d4146ea7a5ab30cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382619997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfe0fbd17c3c5292493baa6c92231a9d4890c3999018fc38ceda814289e84be`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:26:45 GMT
ENV RC_VERSION=6.7.7
# Fri, 27 Sep 2024 05:26:45 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:28:40 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:28:48 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:28:48 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:28:48 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:28:48 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:28:49 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b581c52bf4d633e81ff5b6a25bf9ae522c93bad947f6b2619b618772890ffd`  
		Last Modified: Fri, 27 Sep 2024 05:36:54 GMT  
		Size: 315.4 MB (315429357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.7.7`

```console
$ docker pull rocket.chat@sha256:e651f33a3390cbbc98eb744453fbfbd0ef42d7e451af39269a68bd343bf34957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.7.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3bc500a2ec9e09cebc1fd3f98398f58068de651a334ad0f4d4146ea7a5ab30cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382619997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfe0fbd17c3c5292493baa6c92231a9d4890c3999018fc38ceda814289e84be`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:26:45 GMT
ENV RC_VERSION=6.7.7
# Fri, 27 Sep 2024 05:26:45 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:28:40 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:28:48 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:28:48 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:28:48 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:28:48 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:28:49 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b581c52bf4d633e81ff5b6a25bf9ae522c93bad947f6b2619b618772890ffd`  
		Last Modified: Fri, 27 Sep 2024 05:36:54 GMT  
		Size: 315.4 MB (315429357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.8`

```console
$ docker pull rocket.chat@sha256:4d1390a968d48f982ac16d062d485111b9574480664bdd855d27ad3948bd83fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:6dcc5f5b4e47825265dcd2c61a5f6623dbbc51677f38d00983c8f3a55b042f18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382739135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc62db83ecc2e611214c8ad26dfcb492081aee6e575cbaeb029497479570292`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:24:21 GMT
ENV RC_VERSION=6.8.5
# Fri, 27 Sep 2024 05:24:21 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:26:24 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:26:29 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:26:29 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:26:29 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:26:29 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:26:29 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55c91c6d01dc3504bb2a0aa32de7c6ad8f1705778dad6ee0c43ca7c5724e13`  
		Last Modified: Fri, 27 Sep 2024 05:35:51 GMT  
		Size: 315.5 MB (315548495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.8.5`

```console
$ docker pull rocket.chat@sha256:4d1390a968d48f982ac16d062d485111b9574480664bdd855d27ad3948bd83fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.8.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:6dcc5f5b4e47825265dcd2c61a5f6623dbbc51677f38d00983c8f3a55b042f18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382739135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc62db83ecc2e611214c8ad26dfcb492081aee6e575cbaeb029497479570292`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:24:21 GMT
ENV RC_VERSION=6.8.5
# Fri, 27 Sep 2024 05:24:21 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:26:24 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:26:29 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:26:29 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:26:29 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:26:29 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:26:29 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55c91c6d01dc3504bb2a0aa32de7c6ad8f1705778dad6ee0c43ca7c5724e13`  
		Last Modified: Fri, 27 Sep 2024 05:35:51 GMT  
		Size: 315.5 MB (315548495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.9`

```console
$ docker pull rocket.chat@sha256:fd69b3926de0b1d9a62fdc014a5ce8e2b99eeeab78fe3eeb604816a519161a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:28cc1fff915a26a23545a407719aca2282a2ea7473c9e4eb0af2accbb307d959
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382767791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ef994a9cab5012ec8673c14a9a5902775f542416dc2ab242c1e8357c505871`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:21:54 GMT
ENV RC_VERSION=6.9.5
# Fri, 27 Sep 2024 05:21:55 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:24:01 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:24:08 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:24:08 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:24:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:24:08 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:24:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f3ded9e18fa133de9b0924751b35c5e62ec39245a926585eb992310391ca63`  
		Last Modified: Fri, 27 Sep 2024 05:34:47 GMT  
		Size: 315.6 MB (315577151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.9.5`

```console
$ docker pull rocket.chat@sha256:fd69b3926de0b1d9a62fdc014a5ce8e2b99eeeab78fe3eeb604816a519161a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.9.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:28cc1fff915a26a23545a407719aca2282a2ea7473c9e4eb0af2accbb307d959
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382767791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ef994a9cab5012ec8673c14a9a5902775f542416dc2ab242c1e8357c505871`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:21:54 GMT
ENV RC_VERSION=6.9.5
# Fri, 27 Sep 2024 05:21:55 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:24:01 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:24:08 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:24:08 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:24:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:24:08 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:24:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f3ded9e18fa133de9b0924751b35c5e62ec39245a926585eb992310391ca63`  
		Last Modified: Fri, 27 Sep 2024 05:34:47 GMT  
		Size: 315.6 MB (315577151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:03ed9438d26b7b5e74d239c3c8fc8e072d1560066e7721f8e1f74cf01b4f1ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:5591debc687299955b91f4cb98b0fc944b7ab59157e6c235226604656adfee97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439189965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe217ee3d2de5b61cb26a77a20e7b7381139d2ab61fb67267e9705049589c0`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_ENV=production
# Fri, 27 Sep 2024 05:21:27 GMT
ENV NODE_VERSION=14.21.3
# Fri, 27 Sep 2024 05:21:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 05:21:54 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Fri, 27 Sep 2024 05:21:54 GMT
VOLUME [/app/uploads]
# Fri, 27 Sep 2024 05:28:54 GMT
ENV RC_VERSION=6.11.1
# Fri, 27 Sep 2024 05:28:54 GMT
WORKDIR /app
# Fri, 27 Sep 2024 05:30:58 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 27 Sep 2024 05:31:07 GMT
USER rocketchat
# Fri, 27 Sep 2024 05:31:07 GMT
WORKDIR /app/bundle
# Fri, 27 Sep 2024 05:31:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Sep 2024 05:31:08 GMT
EXPOSE 3000
# Fri, 27 Sep 2024 05:31:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7c249a8550699826286934b44ed548389fb202788fc3f2eb6dcbde6d31f88`  
		Last Modified: Fri, 27 Sep 2024 05:33:55 GMT  
		Size: 35.8 MB (35760260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69137012da28b71c956d68c606f51acd9b48a4036fdce359afbf3a1c4141dccd`  
		Last Modified: Fri, 27 Sep 2024 05:33:50 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ea88d87cdfd8ec642e860bd03acb3b03f889fbdfc9a7daf451965ecb59b92a`  
		Last Modified: Fri, 27 Sep 2024 05:38:04 GMT  
		Size: 372.0 MB (371999325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

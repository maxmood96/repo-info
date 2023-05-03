<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:5`](#rocketchat5)
-	[`rocket.chat:5.2`](#rocketchat52)
-	[`rocket.chat:5.2.2`](#rocketchat522)
-	[`rocket.chat:5.3`](#rocketchat53)
-	[`rocket.chat:5.3.6`](#rocketchat536)
-	[`rocket.chat:5.4`](#rocketchat54)
-	[`rocket.chat:5.4.4`](#rocketchat544)
-	[`rocket.chat:6`](#rocketchat6)
-	[`rocket.chat:6.0`](#rocketchat60)
-	[`rocket.chat:6.0.0`](#rocketchat600)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:5`

```console
$ docker pull rocket.chat@sha256:a243759b48f4edc5a247285795b39c869934f956558ed3bc42bec7709b3d0b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:941c8bed8316b09340885e75cb40eed9cdb972babd0114cfdacb295540fcdb66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301721004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc65e1ff646b6bd1ad6d847d3a7e1be2ec316167a8f6568ff7414e6d0e040b`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:30:51 GMT
ENV RC_VERSION=5.4.4
# Wed, 03 May 2023 21:30:51 GMT
WORKDIR /app
# Wed, 03 May 2023 21:31:52 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:31:56 GMT
USER rocketchat
# Wed, 03 May 2023 21:31:56 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:31:56 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:31:56 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:31:56 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a24670081ccbec7a8c03243b7cbfe17d380946f6d42ca4468388413e181852`  
		Last Modified: Wed, 03 May 2023 21:36:18 GMT  
		Size: 238.6 MB (238555335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.2`

```console
$ docker pull rocket.chat@sha256:5c989e74560bf68b4810672fbb8bddd51d0b71bca24a172ff3b3256357d1f575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:46d1535a759da395bfbd4266b335e66647313e16bed222e00905e7f20b79edf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291096721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea5e101dbe6640d6b71de389b0b7a16a40decf7b22a467e38039a127121af62`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:33:21 GMT
ENV RC_VERSION=5.2.2
# Wed, 03 May 2023 21:33:21 GMT
WORKDIR /app
# Wed, 03 May 2023 21:34:20 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:34:24 GMT
USER rocketchat
# Wed, 03 May 2023 21:34:24 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:34:24 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:34:24 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:34:24 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b046b434a9086a792172373e599ae5e0dc25bb59120b4cee976eac5e54a146`  
		Last Modified: Wed, 03 May 2023 21:37:56 GMT  
		Size: 227.9 MB (227931052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.2.2`

```console
$ docker pull rocket.chat@sha256:5c989e74560bf68b4810672fbb8bddd51d0b71bca24a172ff3b3256357d1f575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.2.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:46d1535a759da395bfbd4266b335e66647313e16bed222e00905e7f20b79edf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291096721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea5e101dbe6640d6b71de389b0b7a16a40decf7b22a467e38039a127121af62`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:33:21 GMT
ENV RC_VERSION=5.2.2
# Wed, 03 May 2023 21:33:21 GMT
WORKDIR /app
# Wed, 03 May 2023 21:34:20 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:34:24 GMT
USER rocketchat
# Wed, 03 May 2023 21:34:24 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:34:24 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:34:24 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:34:24 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b046b434a9086a792172373e599ae5e0dc25bb59120b4cee976eac5e54a146`  
		Last Modified: Wed, 03 May 2023 21:37:56 GMT  
		Size: 227.9 MB (227931052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.3`

```console
$ docker pull rocket.chat@sha256:3a1bb4194c3ab9d445390d01b841c7f28b51f7f7398d2633aded845a1b276e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:56ec8be18c2c55f067697c3463233733e2991907fc98c889a262386fbfbed1be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292520412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5d12af873b5c943506894970ed8a391225c64aa131f998876cad60f6a708d6`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:32:12 GMT
ENV RC_VERSION=5.3.6
# Wed, 03 May 2023 21:32:12 GMT
WORKDIR /app
# Wed, 03 May 2023 21:33:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:33:14 GMT
USER rocketchat
# Wed, 03 May 2023 21:33:14 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:33:15 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:33:15 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:33:15 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9862e98ede92a51324fa63e1b1af96e022bd71f0bfa126e91dba753e237c58`  
		Last Modified: Wed, 03 May 2023 21:37:08 GMT  
		Size: 229.4 MB (229354743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.3.6`

```console
$ docker pull rocket.chat@sha256:3a1bb4194c3ab9d445390d01b841c7f28b51f7f7398d2633aded845a1b276e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.3.6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:56ec8be18c2c55f067697c3463233733e2991907fc98c889a262386fbfbed1be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292520412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5d12af873b5c943506894970ed8a391225c64aa131f998876cad60f6a708d6`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:32:12 GMT
ENV RC_VERSION=5.3.6
# Wed, 03 May 2023 21:32:12 GMT
WORKDIR /app
# Wed, 03 May 2023 21:33:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:33:14 GMT
USER rocketchat
# Wed, 03 May 2023 21:33:14 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:33:15 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:33:15 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:33:15 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9862e98ede92a51324fa63e1b1af96e022bd71f0bfa126e91dba753e237c58`  
		Last Modified: Wed, 03 May 2023 21:37:08 GMT  
		Size: 229.4 MB (229354743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.4`

```console
$ docker pull rocket.chat@sha256:a243759b48f4edc5a247285795b39c869934f956558ed3bc42bec7709b3d0b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:941c8bed8316b09340885e75cb40eed9cdb972babd0114cfdacb295540fcdb66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301721004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc65e1ff646b6bd1ad6d847d3a7e1be2ec316167a8f6568ff7414e6d0e040b`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:30:51 GMT
ENV RC_VERSION=5.4.4
# Wed, 03 May 2023 21:30:51 GMT
WORKDIR /app
# Wed, 03 May 2023 21:31:52 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:31:56 GMT
USER rocketchat
# Wed, 03 May 2023 21:31:56 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:31:56 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:31:56 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:31:56 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a24670081ccbec7a8c03243b7cbfe17d380946f6d42ca4468388413e181852`  
		Last Modified: Wed, 03 May 2023 21:36:18 GMT  
		Size: 238.6 MB (238555335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.4.4`

```console
$ docker pull rocket.chat@sha256:a243759b48f4edc5a247285795b39c869934f956558ed3bc42bec7709b3d0b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.4.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:941c8bed8316b09340885e75cb40eed9cdb972babd0114cfdacb295540fcdb66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301721004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc65e1ff646b6bd1ad6d847d3a7e1be2ec316167a8f6568ff7414e6d0e040b`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:29:49 GMT
ENV NODE_VERSION=14.19.3
# Wed, 03 May 2023 21:30:50 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:30:50 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:30:51 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:30:51 GMT
ENV RC_VERSION=5.4.4
# Wed, 03 May 2023 21:30:51 GMT
WORKDIR /app
# Wed, 03 May 2023 21:31:52 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:31:56 GMT
USER rocketchat
# Wed, 03 May 2023 21:31:56 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:31:56 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:31:56 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:31:56 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574ecfa49b56ab1e593682145bd89d0e941331828505dc27ca39f1970f50d2c`  
		Last Modified: Wed, 03 May 2023 21:35:42 GMT  
		Size: 36.0 MB (36024903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8248bdba08eabe07d4f039a1eaa9e4bb8e56f29f863be8a3f72c04555b1e4`  
		Last Modified: Wed, 03 May 2023 21:35:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a24670081ccbec7a8c03243b7cbfe17d380946f6d42ca4468388413e181852`  
		Last Modified: Wed, 03 May 2023 21:36:18 GMT  
		Size: 238.6 MB (238555335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6`

```console
$ docker pull rocket.chat@sha256:45be3914c428ad41f10770e94231d18afccca3b54e1e8d9e6c22fc78c1d4e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:829529e26f74c06971436768ee4288ba2f862640495523003a99a92ae568c3f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f15d7758e20f842c7610cc37b55d8560ea9543473f8be5bccf2c0487f183cc`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_VERSION=14.21.2
# Wed, 03 May 2023 21:28:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:28:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:28:36 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:28:36 GMT
ENV RC_VERSION=6.0.0
# Wed, 03 May 2023 21:28:37 GMT
WORKDIR /app
# Wed, 03 May 2023 21:29:40 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:29:45 GMT
USER rocketchat
# Wed, 03 May 2023 21:29:45 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:29:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:29:45 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:29:45 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec545e08243c793623b2a17ed743348ed8a21e369c54c6e6c26b72e5356bc4`  
		Last Modified: Wed, 03 May 2023 21:34:44 GMT  
		Size: 36.5 MB (36530293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c1bb3996637d86b1edefe5f83e13bed32c1ec76722fd9aafc66a3cb297fa2`  
		Last Modified: Wed, 03 May 2023 21:34:38 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7406f10807e0eb602ffd374d027f306901ed1506bb20625eacdbda29c1cb5f`  
		Last Modified: Wed, 03 May 2023 21:35:25 GMT  
		Size: 264.9 MB (264914250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.0`

```console
$ docker pull rocket.chat@sha256:45be3914c428ad41f10770e94231d18afccca3b54e1e8d9e6c22fc78c1d4e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:829529e26f74c06971436768ee4288ba2f862640495523003a99a92ae568c3f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f15d7758e20f842c7610cc37b55d8560ea9543473f8be5bccf2c0487f183cc`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_VERSION=14.21.2
# Wed, 03 May 2023 21:28:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:28:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:28:36 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:28:36 GMT
ENV RC_VERSION=6.0.0
# Wed, 03 May 2023 21:28:37 GMT
WORKDIR /app
# Wed, 03 May 2023 21:29:40 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:29:45 GMT
USER rocketchat
# Wed, 03 May 2023 21:29:45 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:29:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:29:45 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:29:45 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec545e08243c793623b2a17ed743348ed8a21e369c54c6e6c26b72e5356bc4`  
		Last Modified: Wed, 03 May 2023 21:34:44 GMT  
		Size: 36.5 MB (36530293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c1bb3996637d86b1edefe5f83e13bed32c1ec76722fd9aafc66a3cb297fa2`  
		Last Modified: Wed, 03 May 2023 21:34:38 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7406f10807e0eb602ffd374d027f306901ed1506bb20625eacdbda29c1cb5f`  
		Last Modified: Wed, 03 May 2023 21:35:25 GMT  
		Size: 264.9 MB (264914250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.0.0`

```console
$ docker pull rocket.chat@sha256:45be3914c428ad41f10770e94231d18afccca3b54e1e8d9e6c22fc78c1d4e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.0.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:829529e26f74c06971436768ee4288ba2f862640495523003a99a92ae568c3f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f15d7758e20f842c7610cc37b55d8560ea9543473f8be5bccf2c0487f183cc`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_VERSION=14.21.2
# Wed, 03 May 2023 21:28:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:28:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:28:36 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:28:36 GMT
ENV RC_VERSION=6.0.0
# Wed, 03 May 2023 21:28:37 GMT
WORKDIR /app
# Wed, 03 May 2023 21:29:40 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:29:45 GMT
USER rocketchat
# Wed, 03 May 2023 21:29:45 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:29:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:29:45 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:29:45 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec545e08243c793623b2a17ed743348ed8a21e369c54c6e6c26b72e5356bc4`  
		Last Modified: Wed, 03 May 2023 21:34:44 GMT  
		Size: 36.5 MB (36530293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c1bb3996637d86b1edefe5f83e13bed32c1ec76722fd9aafc66a3cb297fa2`  
		Last Modified: Wed, 03 May 2023 21:34:38 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7406f10807e0eb602ffd374d027f306901ed1506bb20625eacdbda29c1cb5f`  
		Last Modified: Wed, 03 May 2023 21:35:25 GMT  
		Size: 264.9 MB (264914250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:45be3914c428ad41f10770e94231d18afccca3b54e1e8d9e6c22fc78c1d4e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:829529e26f74c06971436768ee4288ba2f862640495523003a99a92ae568c3f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f15d7758e20f842c7610cc37b55d8560ea9543473f8be5bccf2c0487f183cc`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_ENV=production
# Wed, 03 May 2023 21:28:11 GMT
ENV NODE_VERSION=14.21.2
# Wed, 03 May 2023 21:28:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 21:28:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 03 May 2023 21:28:36 GMT
VOLUME [/app/uploads]
# Wed, 03 May 2023 21:28:36 GMT
ENV RC_VERSION=6.0.0
# Wed, 03 May 2023 21:28:37 GMT
WORKDIR /app
# Wed, 03 May 2023 21:29:40 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 03 May 2023 21:29:45 GMT
USER rocketchat
# Wed, 03 May 2023 21:29:45 GMT
WORKDIR /app/bundle
# Wed, 03 May 2023 21:29:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 03 May 2023 21:29:45 GMT
EXPOSE 3000
# Wed, 03 May 2023 21:29:45 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec545e08243c793623b2a17ed743348ed8a21e369c54c6e6c26b72e5356bc4`  
		Last Modified: Wed, 03 May 2023 21:34:44 GMT  
		Size: 36.5 MB (36530293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c1bb3996637d86b1edefe5f83e13bed32c1ec76722fd9aafc66a3cb297fa2`  
		Last Modified: Wed, 03 May 2023 21:34:38 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7406f10807e0eb602ffd374d027f306901ed1506bb20625eacdbda29c1cb5f`  
		Last Modified: Wed, 03 May 2023 21:35:25 GMT  
		Size: 264.9 MB (264914250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

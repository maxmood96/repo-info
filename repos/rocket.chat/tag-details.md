<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:2`](#rocketchat2)
-	[`rocket.chat:2.4`](#rocketchat24)
-	[`rocket.chat:2.4.14`](#rocketchat2414)
-	[`rocket.chat:3`](#rocketchat3)
-	[`rocket.chat:3.16`](#rocketchat316)
-	[`rocket.chat:3.16.4`](#rocketchat3164)
-	[`rocket.chat:3.17`](#rocketchat317)
-	[`rocket.chat:3.17.2`](#rocketchat3172)
-	[`rocket.chat:3.18`](#rocketchat318)
-	[`rocket.chat:3.18.0`](#rocketchat3180)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:2`

```console
$ docker pull rocket.chat@sha256:82ac46f9f50018501c5bd16ff02151009a2366560753e761e6a318a4512ccc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a298ad3f97cde500f1e2d0acb831e65cac2f37afa00262a72680bb6d0e5881c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216766353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa0588e8a7c8995ca42d62984ec95ee6fbce273c69e1e0cc44985b43dd6da31`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:46:20 GMT
ENV NODE_VERSION=8.17.0
# Tue, 17 Aug 2021 14:46:58 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:46:59 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:47:00 GMT
VOLUME [/app/uploads]
# Tue, 17 Aug 2021 14:47:00 GMT
ENV RC_VERSION=2.4.14
# Tue, 17 Aug 2021 14:47:00 GMT
WORKDIR /app
# Tue, 17 Aug 2021 14:47:55 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 17 Aug 2021 14:47:58 GMT
USER rocketchat
# Tue, 17 Aug 2021 14:47:58 GMT
WORKDIR /app/bundle
# Tue, 17 Aug 2021 14:47:58 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 17 Aug 2021 14:47:59 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:47:59 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f235b956893eb287e32eb9c5174465fdddc84ea193aa0020eeaa64d090bca`  
		Last Modified: Tue, 17 Aug 2021 14:52:31 GMT  
		Size: 19.7 MB (19729848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe43bb9b98e4dba734ebce576584564d7d968a72ba342df0415713798fecabc`  
		Last Modified: Tue, 17 Aug 2021 14:52:27 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bab92b9a9e8853d958982e61b6a31956004453fc57b45033dc8ed4f6631e56`  
		Last Modified: Tue, 17 Aug 2021 14:53:04 GMT  
		Size: 169.9 MB (169888715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:2.4`

```console
$ docker pull rocket.chat@sha256:82ac46f9f50018501c5bd16ff02151009a2366560753e761e6a318a4512ccc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:2.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a298ad3f97cde500f1e2d0acb831e65cac2f37afa00262a72680bb6d0e5881c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216766353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa0588e8a7c8995ca42d62984ec95ee6fbce273c69e1e0cc44985b43dd6da31`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:46:20 GMT
ENV NODE_VERSION=8.17.0
# Tue, 17 Aug 2021 14:46:58 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:46:59 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:47:00 GMT
VOLUME [/app/uploads]
# Tue, 17 Aug 2021 14:47:00 GMT
ENV RC_VERSION=2.4.14
# Tue, 17 Aug 2021 14:47:00 GMT
WORKDIR /app
# Tue, 17 Aug 2021 14:47:55 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 17 Aug 2021 14:47:58 GMT
USER rocketchat
# Tue, 17 Aug 2021 14:47:58 GMT
WORKDIR /app/bundle
# Tue, 17 Aug 2021 14:47:58 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 17 Aug 2021 14:47:59 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:47:59 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f235b956893eb287e32eb9c5174465fdddc84ea193aa0020eeaa64d090bca`  
		Last Modified: Tue, 17 Aug 2021 14:52:31 GMT  
		Size: 19.7 MB (19729848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe43bb9b98e4dba734ebce576584564d7d968a72ba342df0415713798fecabc`  
		Last Modified: Tue, 17 Aug 2021 14:52:27 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bab92b9a9e8853d958982e61b6a31956004453fc57b45033dc8ed4f6631e56`  
		Last Modified: Tue, 17 Aug 2021 14:53:04 GMT  
		Size: 169.9 MB (169888715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:2.4.14`

```console
$ docker pull rocket.chat@sha256:82ac46f9f50018501c5bd16ff02151009a2366560753e761e6a318a4512ccc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:2.4.14` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a298ad3f97cde500f1e2d0acb831e65cac2f37afa00262a72680bb6d0e5881c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216766353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa0588e8a7c8995ca42d62984ec95ee6fbce273c69e1e0cc44985b43dd6da31`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:46:20 GMT
ENV NODE_VERSION=8.17.0
# Tue, 17 Aug 2021 14:46:58 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:46:59 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:47:00 GMT
VOLUME [/app/uploads]
# Tue, 17 Aug 2021 14:47:00 GMT
ENV RC_VERSION=2.4.14
# Tue, 17 Aug 2021 14:47:00 GMT
WORKDIR /app
# Tue, 17 Aug 2021 14:47:55 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 17 Aug 2021 14:47:58 GMT
USER rocketchat
# Tue, 17 Aug 2021 14:47:58 GMT
WORKDIR /app/bundle
# Tue, 17 Aug 2021 14:47:58 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 17 Aug 2021 14:47:59 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:47:59 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f235b956893eb287e32eb9c5174465fdddc84ea193aa0020eeaa64d090bca`  
		Last Modified: Tue, 17 Aug 2021 14:52:31 GMT  
		Size: 19.7 MB (19729848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe43bb9b98e4dba734ebce576584564d7d968a72ba342df0415713798fecabc`  
		Last Modified: Tue, 17 Aug 2021 14:52:27 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bab92b9a9e8853d958982e61b6a31956004453fc57b45033dc8ed4f6631e56`  
		Last Modified: Tue, 17 Aug 2021 14:53:04 GMT  
		Size: 169.9 MB (169888715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3`

```console
$ docker pull rocket.chat@sha256:a46d95404820b2a63478476e21e378e1ca63c2207267e6a34a579c3ecc1c25e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:bc384ddca47c980c0a9509fa5779a22792d313b928c5d0a10cdd4e52a7eef42c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232177221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140cb6e11bf6114e4bfd2a86f1fda48e2deb54a2d503defc0e27e1c3d4497fd4`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_VERSION=12.22.1
# Tue, 17 Aug 2021 14:39:41 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:39:42 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:39:42 GMT
VOLUME [/app/uploads]
# Fri, 27 Aug 2021 17:46:17 GMT
ENV RC_VERSION=3.17.2
# Fri, 27 Aug 2021 17:46:18 GMT
WORKDIR /app
# Fri, 27 Aug 2021 17:47:36 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Fri, 27 Aug 2021 17:47:41 GMT
USER rocketchat
# Fri, 27 Aug 2021 17:47:42 GMT
WORKDIR /app/bundle
# Fri, 27 Aug 2021 17:47:42 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Aug 2021 17:47:42 GMT
EXPOSE 3000
# Fri, 27 Aug 2021 17:47:42 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b94d4af2fa7259aacce034bdc13bee3fee2cba993ea04374d7ec3ea3c76a3a`  
		Last Modified: Tue, 17 Aug 2021 14:48:44 GMT  
		Size: 24.1 MB (24084992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c07992f7a9e935e2ec88479f14093c2decc42f657ec0a60aaabf312879a08`  
		Last Modified: Tue, 17 Aug 2021 14:48:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217738673e209fe41fd30370f75a65a8dff6f3d54a177536ed6fbe5efd3ff310`  
		Last Modified: Fri, 27 Aug 2021 17:49:03 GMT  
		Size: 180.9 MB (180944437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.16`

```console
$ docker pull rocket.chat@sha256:fcd9a37c94c6f9d710f8e0fc57d958072609bed42f442c6dcf2a2ff070045c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:3.16` - linux; amd64

```console
$ docker pull rocket.chat@sha256:32130db2c20d4ce0d048e4fc3c5910ff83c1308462d93cc808f6da644eb92001
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224397920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e579d3a0abf71c33d50cffbe44fa3c3ed8fa1b844ac25aec822fe16e91d056c2`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_VERSION=12.22.1
# Tue, 17 Aug 2021 14:39:41 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:39:42 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:39:42 GMT
VOLUME [/app/uploads]
# Tue, 17 Aug 2021 14:41:33 GMT
ENV RC_VERSION=3.16.4
# Tue, 17 Aug 2021 14:41:34 GMT
WORKDIR /app
# Tue, 17 Aug 2021 14:42:59 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 17 Aug 2021 14:43:05 GMT
USER rocketchat
# Tue, 17 Aug 2021 14:43:05 GMT
WORKDIR /app/bundle
# Tue, 17 Aug 2021 14:43:05 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 17 Aug 2021 14:43:06 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:43:06 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b94d4af2fa7259aacce034bdc13bee3fee2cba993ea04374d7ec3ea3c76a3a`  
		Last Modified: Tue, 17 Aug 2021 14:48:44 GMT  
		Size: 24.1 MB (24084992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c07992f7a9e935e2ec88479f14093c2decc42f657ec0a60aaabf312879a08`  
		Last Modified: Tue, 17 Aug 2021 14:48:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42512850487e004fecbdd0a911b8de69dabfb1aae38757cadc3e1136bd178a93`  
		Last Modified: Tue, 17 Aug 2021 14:50:27 GMT  
		Size: 173.2 MB (173165136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.16.4`

```console
$ docker pull rocket.chat@sha256:fcd9a37c94c6f9d710f8e0fc57d958072609bed42f442c6dcf2a2ff070045c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:3.16.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:32130db2c20d4ce0d048e4fc3c5910ff83c1308462d93cc808f6da644eb92001
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224397920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e579d3a0abf71c33d50cffbe44fa3c3ed8fa1b844ac25aec822fe16e91d056c2`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_VERSION=12.22.1
# Tue, 17 Aug 2021 14:39:41 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:39:42 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:39:42 GMT
VOLUME [/app/uploads]
# Tue, 17 Aug 2021 14:41:33 GMT
ENV RC_VERSION=3.16.4
# Tue, 17 Aug 2021 14:41:34 GMT
WORKDIR /app
# Tue, 17 Aug 2021 14:42:59 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Tue, 17 Aug 2021 14:43:05 GMT
USER rocketchat
# Tue, 17 Aug 2021 14:43:05 GMT
WORKDIR /app/bundle
# Tue, 17 Aug 2021 14:43:05 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 17 Aug 2021 14:43:06 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:43:06 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b94d4af2fa7259aacce034bdc13bee3fee2cba993ea04374d7ec3ea3c76a3a`  
		Last Modified: Tue, 17 Aug 2021 14:48:44 GMT  
		Size: 24.1 MB (24084992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c07992f7a9e935e2ec88479f14093c2decc42f657ec0a60aaabf312879a08`  
		Last Modified: Tue, 17 Aug 2021 14:48:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42512850487e004fecbdd0a911b8de69dabfb1aae38757cadc3e1136bd178a93`  
		Last Modified: Tue, 17 Aug 2021 14:50:27 GMT  
		Size: 173.2 MB (173165136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.17`

```console
$ docker pull rocket.chat@sha256:a46d95404820b2a63478476e21e378e1ca63c2207267e6a34a579c3ecc1c25e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:3.17` - linux; amd64

```console
$ docker pull rocket.chat@sha256:bc384ddca47c980c0a9509fa5779a22792d313b928c5d0a10cdd4e52a7eef42c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232177221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140cb6e11bf6114e4bfd2a86f1fda48e2deb54a2d503defc0e27e1c3d4497fd4`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_VERSION=12.22.1
# Tue, 17 Aug 2021 14:39:41 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:39:42 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:39:42 GMT
VOLUME [/app/uploads]
# Fri, 27 Aug 2021 17:46:17 GMT
ENV RC_VERSION=3.17.2
# Fri, 27 Aug 2021 17:46:18 GMT
WORKDIR /app
# Fri, 27 Aug 2021 17:47:36 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Fri, 27 Aug 2021 17:47:41 GMT
USER rocketchat
# Fri, 27 Aug 2021 17:47:42 GMT
WORKDIR /app/bundle
# Fri, 27 Aug 2021 17:47:42 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Aug 2021 17:47:42 GMT
EXPOSE 3000
# Fri, 27 Aug 2021 17:47:42 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b94d4af2fa7259aacce034bdc13bee3fee2cba993ea04374d7ec3ea3c76a3a`  
		Last Modified: Tue, 17 Aug 2021 14:48:44 GMT  
		Size: 24.1 MB (24084992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c07992f7a9e935e2ec88479f14093c2decc42f657ec0a60aaabf312879a08`  
		Last Modified: Tue, 17 Aug 2021 14:48:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217738673e209fe41fd30370f75a65a8dff6f3d54a177536ed6fbe5efd3ff310`  
		Last Modified: Fri, 27 Aug 2021 17:49:03 GMT  
		Size: 180.9 MB (180944437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.17.2`

```console
$ docker pull rocket.chat@sha256:a46d95404820b2a63478476e21e378e1ca63c2207267e6a34a579c3ecc1c25e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:3.17.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:bc384ddca47c980c0a9509fa5779a22792d313b928c5d0a10cdd4e52a7eef42c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232177221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140cb6e11bf6114e4bfd2a86f1fda48e2deb54a2d503defc0e27e1c3d4497fd4`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_VERSION=12.22.1
# Tue, 17 Aug 2021 14:39:41 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:39:42 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:39:42 GMT
VOLUME [/app/uploads]
# Fri, 27 Aug 2021 17:46:17 GMT
ENV RC_VERSION=3.17.2
# Fri, 27 Aug 2021 17:46:18 GMT
WORKDIR /app
# Fri, 27 Aug 2021 17:47:36 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Fri, 27 Aug 2021 17:47:41 GMT
USER rocketchat
# Fri, 27 Aug 2021 17:47:42 GMT
WORKDIR /app/bundle
# Fri, 27 Aug 2021 17:47:42 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Aug 2021 17:47:42 GMT
EXPOSE 3000
# Fri, 27 Aug 2021 17:47:42 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b94d4af2fa7259aacce034bdc13bee3fee2cba993ea04374d7ec3ea3c76a3a`  
		Last Modified: Tue, 17 Aug 2021 14:48:44 GMT  
		Size: 24.1 MB (24084992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c07992f7a9e935e2ec88479f14093c2decc42f657ec0a60aaabf312879a08`  
		Last Modified: Tue, 17 Aug 2021 14:48:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217738673e209fe41fd30370f75a65a8dff6f3d54a177536ed6fbe5efd3ff310`  
		Last Modified: Fri, 27 Aug 2021 17:49:03 GMT  
		Size: 180.9 MB (180944437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.18`

**does not exist** (yet?)

## `rocket.chat:3.18.0`

**does not exist** (yet?)

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:a46d95404820b2a63478476e21e378e1ca63c2207267e6a34a579c3ecc1c25e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:bc384ddca47c980c0a9509fa5779a22792d313b928c5d0a10cdd4e52a7eef42c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232177221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140cb6e11bf6114e4bfd2a86f1fda48e2deb54a2d503defc0e27e1c3d4497fd4`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_ENV=production
# Tue, 17 Aug 2021 14:39:07 GMT
ENV NODE_VERSION=12.22.1
# Tue, 17 Aug 2021 14:39:41 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:39:42 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Tue, 17 Aug 2021 14:39:42 GMT
VOLUME [/app/uploads]
# Fri, 27 Aug 2021 17:46:17 GMT
ENV RC_VERSION=3.17.2
# Fri, 27 Aug 2021 17:46:18 GMT
WORKDIR /app
# Fri, 27 Aug 2021 17:47:36 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg && rm -rf /var/lib/apt/lists/* &&  gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Fri, 27 Aug 2021 17:47:41 GMT
USER rocketchat
# Fri, 27 Aug 2021 17:47:42 GMT
WORKDIR /app/bundle
# Fri, 27 Aug 2021 17:47:42 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 27 Aug 2021 17:47:42 GMT
EXPOSE 3000
# Fri, 27 Aug 2021 17:47:42 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b94d4af2fa7259aacce034bdc13bee3fee2cba993ea04374d7ec3ea3c76a3a`  
		Last Modified: Tue, 17 Aug 2021 14:48:44 GMT  
		Size: 24.1 MB (24084992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c07992f7a9e935e2ec88479f14093c2decc42f657ec0a60aaabf312879a08`  
		Last Modified: Tue, 17 Aug 2021 14:48:37 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217738673e209fe41fd30370f75a65a8dff6f3d54a177536ed6fbe5efd3ff310`  
		Last Modified: Fri, 27 Aug 2021 17:49:03 GMT  
		Size: 180.9 MB (180944437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

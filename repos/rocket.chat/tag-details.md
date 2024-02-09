<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:6`](#rocketchat6)
-	[`rocket.chat:6.3`](#rocketchat63)
-	[`rocket.chat:6.3.12`](#rocketchat6312)
-	[`rocket.chat:6.4`](#rocketchat64)
-	[`rocket.chat:6.4.9`](#rocketchat649)
-	[`rocket.chat:6.5`](#rocketchat65)
-	[`rocket.chat:6.5.3`](#rocketchat653)
-	[`rocket.chat:6.6`](#rocketchat66)
-	[`rocket.chat:6.6.0`](#rocketchat660)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:6`

```console
$ docker pull rocket.chat@sha256:e2bf24c26532eb8b5abc7f1e365008b1bacbc198230a826528930f6008d40d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:0e23baf547796bb7e3e2c3da1b85d9011e945b7cd65533483125284e78bf2936
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374331914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44e5635b96eb751d3d878fa3343223b6f534d924124a8441ff24d4a2cc5a2c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Fri, 09 Feb 2024 03:44:46 GMT
ENV RC_VERSION=6.6.0
# Fri, 09 Feb 2024 03:44:46 GMT
WORKDIR /app
# Fri, 09 Feb 2024 03:46:01 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 09 Feb 2024 03:46:07 GMT
USER rocketchat
# Fri, 09 Feb 2024 03:46:07 GMT
WORKDIR /app/bundle
# Fri, 09 Feb 2024 03:46:07 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 09 Feb 2024 03:46:08 GMT
EXPOSE 3000
# Fri, 09 Feb 2024 03:46:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fecaf849be27f524e20049504a3e0ec57e159e387a2486bd62bd2ba1b7853c`  
		Last Modified: Fri, 09 Feb 2024 03:49:10 GMT  
		Size: 307.2 MB (307150053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.3`

```console
$ docker pull rocket.chat@sha256:90e70343200c45f91a1ba87f0b580f2ea89035f9466f2ae53c42b083221c872e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:99026132c3792909e28e21e4d23db6061d2106465c07d05052dead58f07dca10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322157646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c0aab01c569c55e2e1e02b4310285514d7c69a8a05215d9f60c00a1e39f53e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:03 GMT
ADD file:a857ebb18123e76fc79a7d720dfdcc496ba12a79af323564b965627d399a5b04 in / 
# Wed, 31 Jan 2024 22:36:04 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:27:42 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:27:42 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:28:08 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:28:09 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:28:09 GMT
VOLUME [/app/uploads]
# Thu, 01 Feb 2024 06:28:09 GMT
ENV RC_VERSION=6.3.12
# Thu, 01 Feb 2024 06:28:09 GMT
WORKDIR /app
# Thu, 01 Feb 2024 06:29:25 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Thu, 01 Feb 2024 06:29:28 GMT
USER rocketchat
# Thu, 01 Feb 2024 06:29:28 GMT
WORKDIR /app/bundle
# Thu, 01 Feb 2024 06:29:28 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 01 Feb 2024 06:29:28 GMT
EXPOSE 3000
# Thu, 01 Feb 2024 06:29:28 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b992ca815489079dcc6d19cf381c63d057e1b924edd453734f694be5ee23dfd9`  
		Last Modified: Wed, 31 Jan 2024 22:41:30 GMT  
		Size: 27.2 MB (27188593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c5e7b3e3237ce18e858bea46cd7e1ebe6ae0a74f9e3133f0419c853719bd84`  
		Last Modified: Thu, 01 Feb 2024 06:32:01 GMT  
		Size: 35.7 MB (35734374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa19d30ad7c0ee83e49be74b4dd65fe5684a15dcc5097f05ab772f4259acc7bb`  
		Last Modified: Thu, 01 Feb 2024 06:31:55 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3000d5a49f5daab5c0fd412e76d457375759fcac30c1bcc7186d109cdcfe7129`  
		Last Modified: Thu, 01 Feb 2024 06:32:42 GMT  
		Size: 259.2 MB (259232873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.3.12`

```console
$ docker pull rocket.chat@sha256:90e70343200c45f91a1ba87f0b580f2ea89035f9466f2ae53c42b083221c872e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.3.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:99026132c3792909e28e21e4d23db6061d2106465c07d05052dead58f07dca10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322157646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c0aab01c569c55e2e1e02b4310285514d7c69a8a05215d9f60c00a1e39f53e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:03 GMT
ADD file:a857ebb18123e76fc79a7d720dfdcc496ba12a79af323564b965627d399a5b04 in / 
# Wed, 31 Jan 2024 22:36:04 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:27:42 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:27:42 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:28:08 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:28:09 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:28:09 GMT
VOLUME [/app/uploads]
# Thu, 01 Feb 2024 06:28:09 GMT
ENV RC_VERSION=6.3.12
# Thu, 01 Feb 2024 06:28:09 GMT
WORKDIR /app
# Thu, 01 Feb 2024 06:29:25 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Thu, 01 Feb 2024 06:29:28 GMT
USER rocketchat
# Thu, 01 Feb 2024 06:29:28 GMT
WORKDIR /app/bundle
# Thu, 01 Feb 2024 06:29:28 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 01 Feb 2024 06:29:28 GMT
EXPOSE 3000
# Thu, 01 Feb 2024 06:29:28 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b992ca815489079dcc6d19cf381c63d057e1b924edd453734f694be5ee23dfd9`  
		Last Modified: Wed, 31 Jan 2024 22:41:30 GMT  
		Size: 27.2 MB (27188593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c5e7b3e3237ce18e858bea46cd7e1ebe6ae0a74f9e3133f0419c853719bd84`  
		Last Modified: Thu, 01 Feb 2024 06:32:01 GMT  
		Size: 35.7 MB (35734374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa19d30ad7c0ee83e49be74b4dd65fe5684a15dcc5097f05ab772f4259acc7bb`  
		Last Modified: Thu, 01 Feb 2024 06:31:55 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3000d5a49f5daab5c0fd412e76d457375759fcac30c1bcc7186d109cdcfe7129`  
		Last Modified: Thu, 01 Feb 2024 06:32:42 GMT  
		Size: 259.2 MB (259232873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.4`

```console
$ docker pull rocket.chat@sha256:20e3a21e820935858781c42256420fc9ec73078d4b6888a8d26a4bf8ffb2f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:90b846ae69f6ea0aa49791e692be55f5bc135eb419b51f588ffee3caa9fafdf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364202125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba3832114e80ab21bf74b927d37bd5d3e5d11c6b21a655d0ddf9b53cfb8f82c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Thu, 01 Feb 2024 06:26:03 GMT
ENV RC_VERSION=6.4.9
# Thu, 01 Feb 2024 06:26:03 GMT
WORKDIR /app
# Thu, 01 Feb 2024 06:27:22 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Thu, 01 Feb 2024 06:27:28 GMT
USER rocketchat
# Thu, 01 Feb 2024 06:27:28 GMT
WORKDIR /app/bundle
# Thu, 01 Feb 2024 06:27:28 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 01 Feb 2024 06:27:28 GMT
EXPOSE 3000
# Thu, 01 Feb 2024 06:27:28 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe2fba52af61ef2039cd101ef3420ecbdb60b13f75817e246fd4996a83e37e`  
		Last Modified: Thu, 01 Feb 2024 06:31:46 GMT  
		Size: 297.0 MB (297020264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.4.9`

```console
$ docker pull rocket.chat@sha256:20e3a21e820935858781c42256420fc9ec73078d4b6888a8d26a4bf8ffb2f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.4.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:90b846ae69f6ea0aa49791e692be55f5bc135eb419b51f588ffee3caa9fafdf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364202125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba3832114e80ab21bf74b927d37bd5d3e5d11c6b21a655d0ddf9b53cfb8f82c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Thu, 01 Feb 2024 06:26:03 GMT
ENV RC_VERSION=6.4.9
# Thu, 01 Feb 2024 06:26:03 GMT
WORKDIR /app
# Thu, 01 Feb 2024 06:27:22 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Thu, 01 Feb 2024 06:27:28 GMT
USER rocketchat
# Thu, 01 Feb 2024 06:27:28 GMT
WORKDIR /app/bundle
# Thu, 01 Feb 2024 06:27:28 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 01 Feb 2024 06:27:28 GMT
EXPOSE 3000
# Thu, 01 Feb 2024 06:27:28 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe2fba52af61ef2039cd101ef3420ecbdb60b13f75817e246fd4996a83e37e`  
		Last Modified: Thu, 01 Feb 2024 06:31:46 GMT  
		Size: 297.0 MB (297020264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.5`

```console
$ docker pull rocket.chat@sha256:50e2b237466c01ab8f4c26d2c74101a58235917f57a9deacb4f18a2d9a3c9484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:35a8c8c1a3355374320b28c3dc2a1e20017d7afb27e026028b643bf46dd7957c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (374961705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e30ec1ccc9fce703f3c6b6fb39680b842d51812634c2ec32c07d2b0a9586ea`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Fri, 09 Feb 2024 03:46:24 GMT
ENV RC_VERSION=6.5.3
# Fri, 09 Feb 2024 03:46:24 GMT
WORKDIR /app
# Fri, 09 Feb 2024 03:47:42 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 09 Feb 2024 03:47:49 GMT
USER rocketchat
# Fri, 09 Feb 2024 03:47:49 GMT
WORKDIR /app/bundle
# Fri, 09 Feb 2024 03:47:49 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 09 Feb 2024 03:47:49 GMT
EXPOSE 3000
# Fri, 09 Feb 2024 03:47:49 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67151d202786014c657002104edee521a2d8ad6843241a155f503782eaf843c7`  
		Last Modified: Fri, 09 Feb 2024 03:50:18 GMT  
		Size: 307.8 MB (307779844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.5.3`

```console
$ docker pull rocket.chat@sha256:50e2b237466c01ab8f4c26d2c74101a58235917f57a9deacb4f18a2d9a3c9484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.5.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:35a8c8c1a3355374320b28c3dc2a1e20017d7afb27e026028b643bf46dd7957c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (374961705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e30ec1ccc9fce703f3c6b6fb39680b842d51812634c2ec32c07d2b0a9586ea`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Fri, 09 Feb 2024 03:46:24 GMT
ENV RC_VERSION=6.5.3
# Fri, 09 Feb 2024 03:46:24 GMT
WORKDIR /app
# Fri, 09 Feb 2024 03:47:42 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 09 Feb 2024 03:47:49 GMT
USER rocketchat
# Fri, 09 Feb 2024 03:47:49 GMT
WORKDIR /app/bundle
# Fri, 09 Feb 2024 03:47:49 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 09 Feb 2024 03:47:49 GMT
EXPOSE 3000
# Fri, 09 Feb 2024 03:47:49 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67151d202786014c657002104edee521a2d8ad6843241a155f503782eaf843c7`  
		Last Modified: Fri, 09 Feb 2024 03:50:18 GMT  
		Size: 307.8 MB (307779844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.6`

```console
$ docker pull rocket.chat@sha256:e2bf24c26532eb8b5abc7f1e365008b1bacbc198230a826528930f6008d40d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:0e23baf547796bb7e3e2c3da1b85d9011e945b7cd65533483125284e78bf2936
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374331914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44e5635b96eb751d3d878fa3343223b6f534d924124a8441ff24d4a2cc5a2c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Fri, 09 Feb 2024 03:44:46 GMT
ENV RC_VERSION=6.6.0
# Fri, 09 Feb 2024 03:44:46 GMT
WORKDIR /app
# Fri, 09 Feb 2024 03:46:01 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 09 Feb 2024 03:46:07 GMT
USER rocketchat
# Fri, 09 Feb 2024 03:46:07 GMT
WORKDIR /app/bundle
# Fri, 09 Feb 2024 03:46:07 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 09 Feb 2024 03:46:08 GMT
EXPOSE 3000
# Fri, 09 Feb 2024 03:46:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fecaf849be27f524e20049504a3e0ec57e159e387a2486bd62bd2ba1b7853c`  
		Last Modified: Fri, 09 Feb 2024 03:49:10 GMT  
		Size: 307.2 MB (307150053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.6.0`

```console
$ docker pull rocket.chat@sha256:e2bf24c26532eb8b5abc7f1e365008b1bacbc198230a826528930f6008d40d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.6.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:0e23baf547796bb7e3e2c3da1b85d9011e945b7cd65533483125284e78bf2936
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374331914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44e5635b96eb751d3d878fa3343223b6f534d924124a8441ff24d4a2cc5a2c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Fri, 09 Feb 2024 03:44:46 GMT
ENV RC_VERSION=6.6.0
# Fri, 09 Feb 2024 03:44:46 GMT
WORKDIR /app
# Fri, 09 Feb 2024 03:46:01 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 09 Feb 2024 03:46:07 GMT
USER rocketchat
# Fri, 09 Feb 2024 03:46:07 GMT
WORKDIR /app/bundle
# Fri, 09 Feb 2024 03:46:07 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 09 Feb 2024 03:46:08 GMT
EXPOSE 3000
# Fri, 09 Feb 2024 03:46:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fecaf849be27f524e20049504a3e0ec57e159e387a2486bd62bd2ba1b7853c`  
		Last Modified: Fri, 09 Feb 2024 03:49:10 GMT  
		Size: 307.2 MB (307150053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:e2bf24c26532eb8b5abc7f1e365008b1bacbc198230a826528930f6008d40d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:0e23baf547796bb7e3e2c3da1b85d9011e945b7cd65533483125284e78bf2936
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374331914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44e5635b96eb751d3d878fa3343223b6f534d924124a8441ff24d4a2cc5a2c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_ENV=production
# Thu, 01 Feb 2024 06:24:09 GMT
ENV NODE_VERSION=14.21.3
# Thu, 01 Feb 2024 06:24:35 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 06:24:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Thu, 01 Feb 2024 06:24:36 GMT
VOLUME [/app/uploads]
# Fri, 09 Feb 2024 03:44:46 GMT
ENV RC_VERSION=6.6.0
# Fri, 09 Feb 2024 03:44:46 GMT
WORKDIR /app
# Fri, 09 Feb 2024 03:46:01 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Fri, 09 Feb 2024 03:46:07 GMT
USER rocketchat
# Fri, 09 Feb 2024 03:46:07 GMT
WORKDIR /app/bundle
# Fri, 09 Feb 2024 03:46:07 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Fri, 09 Feb 2024 03:46:08 GMT
EXPOSE 3000
# Fri, 09 Feb 2024 03:46:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87593fbbbbd080678cf87316ccf42899e47f86fff9a262a19cdb365941ce2af`  
		Last Modified: Thu, 01 Feb 2024 06:29:49 GMT  
		Size: 35.8 MB (35762221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244b66ed8b19f98f64ccc295a0957fae091097e48ba33cfc2af90e90060a4f8`  
		Last Modified: Thu, 01 Feb 2024 06:29:44 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fecaf849be27f524e20049504a3e0ec57e159e387a2486bd62bd2ba1b7853c`  
		Last Modified: Fri, 09 Feb 2024 03:49:10 GMT  
		Size: 307.2 MB (307150053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

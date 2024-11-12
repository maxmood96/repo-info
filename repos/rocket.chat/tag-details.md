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
$ docker pull rocket.chat@sha256:da72066b6073dca84fb452aff442cc0f83599989b61ad571924ecce3b0bde708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:40f0598f4fb6243730d315f2472173b84683d6ff72be65148fdb20707deaf690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439241255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16272b713c95a269cec0ad224c7b45e68eb5500989872b032398788132ae1075`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.11.1
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13467c5b31558df3be987da2e3d58b9fedd77e74a4e0a8ae47a4fc052bf7e90`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 35.8 MB (35760860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffe2c9daa2c083d276ddd78c94a8aa58f5f8f7fb4c014f29c07b4b94e83c9a`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21927f50d7b987dc99e452bf3d080780077cf3cc49c84dbc44f4396cecc811`  
		Last Modified: Tue, 12 Nov 2024 02:13:10 GMT  
		Size: 372.0 MB (372027079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:38e257418bf7017387529ebb1126ea65d1d373fabe95d552f2921df70e446d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30469e21a13fd15e85b311ae833e078dcae5bfd4fa8a89b812090bfa755be0cf`

```dockerfile
```

-	Layers:
	-	`sha256:941c5696e875de1f7774cd800e2e478c65dc552799c76af98ea5bf8139af5927`  
		Last Modified: Tue, 12 Nov 2024 02:13:03 GMT  
		Size: 22.0 KB (22017 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.10`

```console
$ docker pull rocket.chat@sha256:851525ddcefda82040bfef109cd91e6984e79579b2bf6bb114679a4f0c794362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:1579e881d1f1687263fc7e5dee903dc0dbebc35411e934a5a28a37ebda5c9a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438667848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162c2571c7adb6fd126b3abd02b4b960118de122e04c9f878adf24b9b57c9c9c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.10.4
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c23609a971f040edf8fbb376771efe1a20c3c3d27b4a1251dcdb03568bbf42`  
		Last Modified: Tue, 12 Nov 2024 02:39:57 GMT  
		Size: 35.8 MB (35760854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccccb3ae54e31a821901bce22f365e5ae0694d56fbefa63bf90e74eda1218f16`  
		Last Modified: Tue, 12 Nov 2024 02:39:56 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4363ff74c607ab143f469e3455380832ddf26bfe0a7715adbd90eb2a192ccef`  
		Last Modified: Tue, 12 Nov 2024 02:40:02 GMT  
		Size: 371.5 MB (371453675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.10` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:f2c5dbd095186fd31d4aca965d2c5efb11046f31d6a96fd7c56bf7606df0e019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbd39b06da33a564404eb97a0a684a36d55d2849ca905fd534fff4b89bf4b50`

```dockerfile
```

-	Layers:
	-	`sha256:d32abed26fdc3ebe2341696a019525b3aecd825253603c3cea670ea32f4317d0`  
		Last Modified: Tue, 12 Nov 2024 02:39:57 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.10.4`

```console
$ docker pull rocket.chat@sha256:851525ddcefda82040bfef109cd91e6984e79579b2bf6bb114679a4f0c794362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.10.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:1579e881d1f1687263fc7e5dee903dc0dbebc35411e934a5a28a37ebda5c9a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438667848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162c2571c7adb6fd126b3abd02b4b960118de122e04c9f878adf24b9b57c9c9c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.10.4
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c23609a971f040edf8fbb376771efe1a20c3c3d27b4a1251dcdb03568bbf42`  
		Last Modified: Tue, 12 Nov 2024 02:39:57 GMT  
		Size: 35.8 MB (35760854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccccb3ae54e31a821901bce22f365e5ae0694d56fbefa63bf90e74eda1218f16`  
		Last Modified: Tue, 12 Nov 2024 02:39:56 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4363ff74c607ab143f469e3455380832ddf26bfe0a7715adbd90eb2a192ccef`  
		Last Modified: Tue, 12 Nov 2024 02:40:02 GMT  
		Size: 371.5 MB (371453675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.10.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:f2c5dbd095186fd31d4aca965d2c5efb11046f31d6a96fd7c56bf7606df0e019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbd39b06da33a564404eb97a0a684a36d55d2849ca905fd534fff4b89bf4b50`

```dockerfile
```

-	Layers:
	-	`sha256:d32abed26fdc3ebe2341696a019525b3aecd825253603c3cea670ea32f4317d0`  
		Last Modified: Tue, 12 Nov 2024 02:39:57 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.11`

```console
$ docker pull rocket.chat@sha256:da72066b6073dca84fb452aff442cc0f83599989b61ad571924ecce3b0bde708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.11` - linux; amd64

```console
$ docker pull rocket.chat@sha256:40f0598f4fb6243730d315f2472173b84683d6ff72be65148fdb20707deaf690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439241255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16272b713c95a269cec0ad224c7b45e68eb5500989872b032398788132ae1075`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.11.1
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13467c5b31558df3be987da2e3d58b9fedd77e74a4e0a8ae47a4fc052bf7e90`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 35.8 MB (35760860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffe2c9daa2c083d276ddd78c94a8aa58f5f8f7fb4c014f29c07b4b94e83c9a`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21927f50d7b987dc99e452bf3d080780077cf3cc49c84dbc44f4396cecc811`  
		Last Modified: Tue, 12 Nov 2024 02:13:10 GMT  
		Size: 372.0 MB (372027079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.11` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:38e257418bf7017387529ebb1126ea65d1d373fabe95d552f2921df70e446d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30469e21a13fd15e85b311ae833e078dcae5bfd4fa8a89b812090bfa755be0cf`

```dockerfile
```

-	Layers:
	-	`sha256:941c5696e875de1f7774cd800e2e478c65dc552799c76af98ea5bf8139af5927`  
		Last Modified: Tue, 12 Nov 2024 02:13:03 GMT  
		Size: 22.0 KB (22017 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.11.1`

```console
$ docker pull rocket.chat@sha256:da72066b6073dca84fb452aff442cc0f83599989b61ad571924ecce3b0bde708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.11.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:40f0598f4fb6243730d315f2472173b84683d6ff72be65148fdb20707deaf690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439241255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16272b713c95a269cec0ad224c7b45e68eb5500989872b032398788132ae1075`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.11.1
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13467c5b31558df3be987da2e3d58b9fedd77e74a4e0a8ae47a4fc052bf7e90`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 35.8 MB (35760860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffe2c9daa2c083d276ddd78c94a8aa58f5f8f7fb4c014f29c07b4b94e83c9a`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21927f50d7b987dc99e452bf3d080780077cf3cc49c84dbc44f4396cecc811`  
		Last Modified: Tue, 12 Nov 2024 02:13:10 GMT  
		Size: 372.0 MB (372027079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.11.1` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:38e257418bf7017387529ebb1126ea65d1d373fabe95d552f2921df70e446d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30469e21a13fd15e85b311ae833e078dcae5bfd4fa8a89b812090bfa755be0cf`

```dockerfile
```

-	Layers:
	-	`sha256:941c5696e875de1f7774cd800e2e478c65dc552799c76af98ea5bf8139af5927`  
		Last Modified: Tue, 12 Nov 2024 02:13:03 GMT  
		Size: 22.0 KB (22017 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.7`

```console
$ docker pull rocket.chat@sha256:28d63b31c1b5dc800723ac2aa8b3982892d515318953d1501d3b04a89190c4e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:c2496931d5fe80df4f14f491ad901ace804c42846f368418a883cd31bf4a8312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382631435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0b870a1f4378fc5beb84d8bdb359e515bea1639805f2e483d237dac48d7900`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.7.7
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c4a2735ed5fbf18a8ac73e6fccde8088a873e398791f6e4899d323f5f42430`  
		Last Modified: Tue, 12 Nov 2024 02:39:48 GMT  
		Size: 35.8 MB (35760861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630105d306a719c59198164edaea36c364866d0f24f24ac5441d054b0a3bae71`  
		Last Modified: Tue, 12 Nov 2024 02:39:47 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debe26b0ef284e7ae7f1a3a98973bb4c1dce8daa91e33fd5d0c3ef757ffef2a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:52 GMT  
		Size: 315.4 MB (315417256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:768a9086134e8eded5edca6cd282e89d1099614a243f108721fc192e2cc339d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c11289a07f2f9fae28ad199f7eb5774655f75352852d18c4a736136c302769e`

```dockerfile
```

-	Layers:
	-	`sha256:3ab6dad19d6bbbe818bede61a0358d2af1fca49499431ca71e23af7dd59f2ede`  
		Last Modified: Tue, 12 Nov 2024 02:39:47 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.7.7`

```console
$ docker pull rocket.chat@sha256:28d63b31c1b5dc800723ac2aa8b3982892d515318953d1501d3b04a89190c4e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.7.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:c2496931d5fe80df4f14f491ad901ace804c42846f368418a883cd31bf4a8312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382631435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0b870a1f4378fc5beb84d8bdb359e515bea1639805f2e483d237dac48d7900`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.7.7
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c4a2735ed5fbf18a8ac73e6fccde8088a873e398791f6e4899d323f5f42430`  
		Last Modified: Tue, 12 Nov 2024 02:39:48 GMT  
		Size: 35.8 MB (35760861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630105d306a719c59198164edaea36c364866d0f24f24ac5441d054b0a3bae71`  
		Last Modified: Tue, 12 Nov 2024 02:39:47 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debe26b0ef284e7ae7f1a3a98973bb4c1dce8daa91e33fd5d0c3ef757ffef2a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:52 GMT  
		Size: 315.4 MB (315417256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.7.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:768a9086134e8eded5edca6cd282e89d1099614a243f108721fc192e2cc339d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c11289a07f2f9fae28ad199f7eb5774655f75352852d18c4a736136c302769e`

```dockerfile
```

-	Layers:
	-	`sha256:3ab6dad19d6bbbe818bede61a0358d2af1fca49499431ca71e23af7dd59f2ede`  
		Last Modified: Tue, 12 Nov 2024 02:39:47 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.8`

```console
$ docker pull rocket.chat@sha256:09ce665fa12295a106571b54acec7d3e860fb3d5bb7b12a7813d507d7e9655fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:31bad825e1c8cda1f0a64bdfe25091de1c370dc35010f772946973f235838767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382761431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ed3b9ab3cfc7379ac9d5309e68917f86bef756f5faab4f04f21c3acb50e50c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.8.5
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02a6afffe3b2adb3ba5e4e392f1008be47a34585f850b342cfd67a3e56c8a0`  
		Last Modified: Tue, 12 Nov 2024 02:12:57 GMT  
		Size: 35.8 MB (35760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214327ba81220682aaf79c630f63e584786877af9954c21dbe2656ae40d03b7f`  
		Last Modified: Tue, 12 Nov 2024 02:12:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87e9dd99de56a4afa32327b1c656264fb15039225d42fe345703da63bc4f1e`  
		Last Modified: Tue, 12 Nov 2024 02:13:01 GMT  
		Size: 315.5 MB (315547216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:810e237bb1976246932c41ace86715531c74393869ba941aa78c591d6fc7fbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138960ba8ad04c1892ca1e11751020a6ceb029a1b443de89ffbca75adc4d7256`

```dockerfile
```

-	Layers:
	-	`sha256:177f5a1801fab83080aa0227ccb4d951918c322862a5defd3eed69b590ecb768`  
		Last Modified: Tue, 12 Nov 2024 02:12:56 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.8.5`

```console
$ docker pull rocket.chat@sha256:09ce665fa12295a106571b54acec7d3e860fb3d5bb7b12a7813d507d7e9655fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.8.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:31bad825e1c8cda1f0a64bdfe25091de1c370dc35010f772946973f235838767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382761431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ed3b9ab3cfc7379ac9d5309e68917f86bef756f5faab4f04f21c3acb50e50c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.8.5
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02a6afffe3b2adb3ba5e4e392f1008be47a34585f850b342cfd67a3e56c8a0`  
		Last Modified: Tue, 12 Nov 2024 02:12:57 GMT  
		Size: 35.8 MB (35760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214327ba81220682aaf79c630f63e584786877af9954c21dbe2656ae40d03b7f`  
		Last Modified: Tue, 12 Nov 2024 02:12:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87e9dd99de56a4afa32327b1c656264fb15039225d42fe345703da63bc4f1e`  
		Last Modified: Tue, 12 Nov 2024 02:13:01 GMT  
		Size: 315.5 MB (315547216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.8.5` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:810e237bb1976246932c41ace86715531c74393869ba941aa78c591d6fc7fbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138960ba8ad04c1892ca1e11751020a6ceb029a1b443de89ffbca75adc4d7256`

```dockerfile
```

-	Layers:
	-	`sha256:177f5a1801fab83080aa0227ccb4d951918c322862a5defd3eed69b590ecb768`  
		Last Modified: Tue, 12 Nov 2024 02:12:56 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.9`

```console
$ docker pull rocket.chat@sha256:320ad6d1a49808a018a6bf442301475b289108f5e296b596c3cabb6270acb3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:dc1344feb1a551567d0e99e437ece6fa7b60e85fa8562005010cb8a0798e84ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382778569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a41a6bb6969f0b8f855f37c49dd02aec9fef9ad6bb3fa0ae289aa098f0cce2`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.9.5
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd800992e53c6c8a1176c1a28c9f2a6cfaabe6812523dd8012fb441d8856ef2`  
		Last Modified: Tue, 12 Nov 2024 02:13:10 GMT  
		Size: 35.8 MB (35760820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a006eda5cf8b2657d9d3dc75da054e6b2bfaa95ad8f2f334b164de9df5b758`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec6b58b1d30bea7975e7dc702631a2c69dab70dfdb7d24b53bec46e519d0f58`  
		Last Modified: Tue, 12 Nov 2024 02:13:20 GMT  
		Size: 315.6 MB (315564431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.9` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1ab12de96dde30724b9c859477f6ef8b5ac8eccc91497371e46b9b1a75762bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaefb6faf9e88732a87d848afbb801cdf1eb1d6d3713fd5851cc8a26de633e3`

```dockerfile
```

-	Layers:
	-	`sha256:3b119fa07ffb766eefd3100da87179bd20f707fb4aa0c8a84a9d4a4b56fc281b`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.9.5`

```console
$ docker pull rocket.chat@sha256:320ad6d1a49808a018a6bf442301475b289108f5e296b596c3cabb6270acb3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.9.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:dc1344feb1a551567d0e99e437ece6fa7b60e85fa8562005010cb8a0798e84ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382778569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a41a6bb6969f0b8f855f37c49dd02aec9fef9ad6bb3fa0ae289aa098f0cce2`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.9.5
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd800992e53c6c8a1176c1a28c9f2a6cfaabe6812523dd8012fb441d8856ef2`  
		Last Modified: Tue, 12 Nov 2024 02:13:10 GMT  
		Size: 35.8 MB (35760820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a006eda5cf8b2657d9d3dc75da054e6b2bfaa95ad8f2f334b164de9df5b758`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec6b58b1d30bea7975e7dc702631a2c69dab70dfdb7d24b53bec46e519d0f58`  
		Last Modified: Tue, 12 Nov 2024 02:13:20 GMT  
		Size: 315.6 MB (315564431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.9.5` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1ab12de96dde30724b9c859477f6ef8b5ac8eccc91497371e46b9b1a75762bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaefb6faf9e88732a87d848afbb801cdf1eb1d6d3713fd5851cc8a26de633e3`

```dockerfile
```

-	Layers:
	-	`sha256:3b119fa07ffb766eefd3100da87179bd20f707fb4aa0c8a84a9d4a4b56fc281b`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:da72066b6073dca84fb452aff442cc0f83599989b61ad571924ecce3b0bde708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:40f0598f4fb6243730d315f2472173b84683d6ff72be65148fdb20707deaf690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439241255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16272b713c95a269cec0ad224c7b45e68eb5500989872b032398788132ae1075`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 26 Aug 2024 20:44:53 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_ENV=production
# Mon, 26 Aug 2024 20:44:53 GMT
ENV NODE_VERSION=14.21.3
# Mon, 26 Aug 2024 20:44:53 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
VOLUME [/app/uploads]
# Mon, 26 Aug 2024 20:44:53 GMT
ENV RC_VERSION=6.11.1
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app
# Mon, 26 Aug 2024 20:44:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Mon, 26 Aug 2024 20:44:53 GMT
USER rocketchat
# Mon, 26 Aug 2024 20:44:53 GMT
WORKDIR /app/bundle
# Mon, 26 Aug 2024 20:44:53 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 26 Aug 2024 20:44:53 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 26 Aug 2024 20:44:53 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13467c5b31558df3be987da2e3d58b9fedd77e74a4e0a8ae47a4fc052bf7e90`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 35.8 MB (35760860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffe2c9daa2c083d276ddd78c94a8aa58f5f8f7fb4c014f29c07b4b94e83c9a`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21927f50d7b987dc99e452bf3d080780077cf3cc49c84dbc44f4396cecc811`  
		Last Modified: Tue, 12 Nov 2024 02:13:10 GMT  
		Size: 372.0 MB (372027079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:latest` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:38e257418bf7017387529ebb1126ea65d1d373fabe95d552f2921df70e446d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30469e21a13fd15e85b311ae833e078dcae5bfd4fa8a89b812090bfa755be0cf`

```dockerfile
```

-	Layers:
	-	`sha256:941c5696e875de1f7774cd800e2e478c65dc552799c76af98ea5bf8139af5927`  
		Last Modified: Tue, 12 Nov 2024 02:13:03 GMT  
		Size: 22.0 KB (22017 bytes)  
		MIME: application/vnd.in-toto+json

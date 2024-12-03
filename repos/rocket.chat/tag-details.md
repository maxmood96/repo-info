<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:6`](#rocketchat6)
-	[`rocket.chat:6.10`](#rocketchat610)
-	[`rocket.chat:6.10.7`](#rocketchat6107)
-	[`rocket.chat:6.11`](#rocketchat611)
-	[`rocket.chat:6.11.3`](#rocketchat6113)
-	[`rocket.chat:6.12`](#rocketchat612)
-	[`rocket.chat:6.12.2`](#rocketchat6122)
-	[`rocket.chat:6.13`](#rocketchat613)
-	[`rocket.chat:6.13.0`](#rocketchat6130)
-	[`rocket.chat:6.8`](#rocketchat68)
-	[`rocket.chat:6.8.7`](#rocketchat687)
-	[`rocket.chat:6.9`](#rocketchat69)
-	[`rocket.chat:6.9.7`](#rocketchat697)
-	[`rocket.chat:7`](#rocketchat7)
-	[`rocket.chat:7.0`](#rocketchat70)
-	[`rocket.chat:7.0.0`](#rocketchat700)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:6`

```console
$ docker pull rocket.chat@sha256:b8e96805c94724857987136c5819754e730778d783d035658f28b7be99306842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:ee928f74ed7a0792de78551736b0e3112f1c883b4d5e2a4ed6c901679f3c01c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.5 MB (431485110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972a42fd045513f4a40558e9ccc870e918b6e74b88feb38c7aee7cd29af3d862`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.13.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a8cf69b87a528ddb50eb8bff8e36ee2a1b0b8ad964c62608d30293f67c3875`  
		Last Modified: Tue, 03 Dec 2024 02:17:32 GMT  
		Size: 35.8 MB (35760856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f979b3e51392f54a25bbe89884fc49003cf6d67634b9dad2bd4f9423f73c`  
		Last Modified: Tue, 03 Dec 2024 02:17:30 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce6e4558100fa79847207f4d5f20b7514a6a4951e0ebd28c36c8d9e247ebad1`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 365.5 MB (365469853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:906f0d221ab9c2ab2ca331ff239bfc3ab616f1dfe84e75d6856d63e94055e642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa26b6da4494ba118306e8ef6dbcfe45b22783bcc1e48126b688fa6b77603c`

```dockerfile
```

-	Layers:
	-	`sha256:2de3a922716a6230ad551816817d288ab8d8440485a4fd31a2f7699422f78798`  
		Last Modified: Tue, 03 Dec 2024 02:17:30 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.10`

```console
$ docker pull rocket.chat@sha256:bc42b99648877d10e638c21e1f05c3c1b2e70e0759a834a2cf37832f56ae3569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:7580ac548021cf2c5c035723b9b7965f6993d33db7d6ab175007a6c97896e330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437542320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d803c77869c796170ed5d36057d3d530eb6f1bef425434332b9ed5f857e61df4`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.10.7
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecaae265fa4889663861b62eeb02909e4eedccab5fc52316b77cfee2c79c21f`  
		Last Modified: Tue, 03 Dec 2024 02:17:52 GMT  
		Size: 35.8 MB (35760876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a441d9f27f4d3280190adb45704b4e825040a833c47f0b11e839a2cc5347cdd5`  
		Last Modified: Tue, 03 Dec 2024 02:17:50 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce6cbe6722cfc8e92e2990db9ccd08cf2adad3f8b6ff09635840f1d6530e02d`  
		Last Modified: Tue, 03 Dec 2024 02:17:57 GMT  
		Size: 371.5 MB (371527040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.10` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:e59bc8ebd711e687d3cfd373b9b60edacdd8cbed3aa38b73e45ae03560255a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6bd4ee88cf7dd79f8c8193ae2e426c1502012ec285c60f40d35323ee071cf4`

```dockerfile
```

-	Layers:
	-	`sha256:ada7fb8cb6920ed946345145a50b20c26a3f44ce2811500a603fea84e98d71c1`  
		Last Modified: Tue, 03 Dec 2024 02:17:50 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.10.7`

```console
$ docker pull rocket.chat@sha256:bc42b99648877d10e638c21e1f05c3c1b2e70e0759a834a2cf37832f56ae3569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.10.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:7580ac548021cf2c5c035723b9b7965f6993d33db7d6ab175007a6c97896e330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437542320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d803c77869c796170ed5d36057d3d530eb6f1bef425434332b9ed5f857e61df4`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.10.7
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecaae265fa4889663861b62eeb02909e4eedccab5fc52316b77cfee2c79c21f`  
		Last Modified: Tue, 03 Dec 2024 02:17:52 GMT  
		Size: 35.8 MB (35760876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a441d9f27f4d3280190adb45704b4e825040a833c47f0b11e839a2cc5347cdd5`  
		Last Modified: Tue, 03 Dec 2024 02:17:50 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce6cbe6722cfc8e92e2990db9ccd08cf2adad3f8b6ff09635840f1d6530e02d`  
		Last Modified: Tue, 03 Dec 2024 02:17:57 GMT  
		Size: 371.5 MB (371527040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.10.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:e59bc8ebd711e687d3cfd373b9b60edacdd8cbed3aa38b73e45ae03560255a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6bd4ee88cf7dd79f8c8193ae2e426c1502012ec285c60f40d35323ee071cf4`

```dockerfile
```

-	Layers:
	-	`sha256:ada7fb8cb6920ed946345145a50b20c26a3f44ce2811500a603fea84e98d71c1`  
		Last Modified: Tue, 03 Dec 2024 02:17:50 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.11`

```console
$ docker pull rocket.chat@sha256:8f56adb1b61db877d502fda53d986dd878a946e1821908bfdc8f52c09b98f806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.11` - linux; amd64

```console
$ docker pull rocket.chat@sha256:c4197eb7651ac24c7fab1aaeef888cd4aabb1e6846125d38597441f6087ba111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438113226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba744beb4ca386b2052e208c16c47752980ee0e90e21cf139cf7816dc4c95b6`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.11.3
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1c8e6cb90a29d84dcc8b3c59ad533a681d0f843da75722c57a43bdf725ae6e`  
		Last Modified: Tue, 03 Dec 2024 02:17:19 GMT  
		Size: 35.8 MB (35760860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5110f5d1a15b879b1eb65fa47861bf44299a8aceefdec1c0b1dc5c100963012a`  
		Last Modified: Tue, 03 Dec 2024 02:17:18 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8632f043dda68b4dcc5e260437d53f5d8bd8027794e780bfd400bbc980f92`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 372.1 MB (372097964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.11` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:09357094b4b99bebafd67ae8c34f803469b06fb9444706263bbd02d9c574a4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f97259ae97d512a9cf1fd21e82163f9e4c99d72a35199003f4528e79e0dba3`

```dockerfile
```

-	Layers:
	-	`sha256:b8bbf28162c73f2ee63ef1b5514eefab5d3f70a12564a631248ae8ad0d0c7c0b`  
		Last Modified: Tue, 03 Dec 2024 02:17:18 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.11.3`

```console
$ docker pull rocket.chat@sha256:8f56adb1b61db877d502fda53d986dd878a946e1821908bfdc8f52c09b98f806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.11.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:c4197eb7651ac24c7fab1aaeef888cd4aabb1e6846125d38597441f6087ba111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438113226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba744beb4ca386b2052e208c16c47752980ee0e90e21cf139cf7816dc4c95b6`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.11.3
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1c8e6cb90a29d84dcc8b3c59ad533a681d0f843da75722c57a43bdf725ae6e`  
		Last Modified: Tue, 03 Dec 2024 02:17:19 GMT  
		Size: 35.8 MB (35760860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5110f5d1a15b879b1eb65fa47861bf44299a8aceefdec1c0b1dc5c100963012a`  
		Last Modified: Tue, 03 Dec 2024 02:17:18 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8632f043dda68b4dcc5e260437d53f5d8bd8027794e780bfd400bbc980f92`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 372.1 MB (372097964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.11.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:09357094b4b99bebafd67ae8c34f803469b06fb9444706263bbd02d9c574a4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f97259ae97d512a9cf1fd21e82163f9e4c99d72a35199003f4528e79e0dba3`

```dockerfile
```

-	Layers:
	-	`sha256:b8bbf28162c73f2ee63ef1b5514eefab5d3f70a12564a631248ae8ad0d0c7c0b`  
		Last Modified: Tue, 03 Dec 2024 02:17:18 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.12`

```console
$ docker pull rocket.chat@sha256:18fccce04ffb7ea4554e41a596dc7f86dd1d1606723473090653e16dac0e05b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d7c66b7ce1b07ecd1839bf61f3e85a19a71fbdc680238a2dfaf4af84ffdad9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429100469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39d2bfc0c7a44266db1bd26da114a1358a37b2641bd5ef84ff2fedc7d7dd857`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.12.2
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adf9c3fda9d8177b7b23276bf60edc00d93ac48f43a66d894c767b188c47d2`  
		Last Modified: Tue, 03 Dec 2024 02:17:34 GMT  
		Size: 35.8 MB (35760830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe30c2f6b19081578f28d9ccccf35f862d11a58ba4e0065ce828b1455dbd5525`  
		Last Modified: Tue, 03 Dec 2024 02:17:33 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b455ba65587466177bfaf0228adc7008e18828bc059e9e369618c36ade988c56`  
		Last Modified: Tue, 03 Dec 2024 02:17:40 GMT  
		Size: 363.1 MB (363085236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.12` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:61dedbbed87e155e745136bc90ab054c50a82878da361446c622b0fbd05f176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62a77b525265f1dc94f38153db3d8c559490f23f3b874b4449e9af3624997a1`

```dockerfile
```

-	Layers:
	-	`sha256:4574fe39846755d947dae849c312c7dfdeacc19bd15e34ef6af5f92f9cbb7892`  
		Last Modified: Tue, 03 Dec 2024 02:17:33 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.12.2`

```console
$ docker pull rocket.chat@sha256:18fccce04ffb7ea4554e41a596dc7f86dd1d1606723473090653e16dac0e05b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.12.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d7c66b7ce1b07ecd1839bf61f3e85a19a71fbdc680238a2dfaf4af84ffdad9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429100469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39d2bfc0c7a44266db1bd26da114a1358a37b2641bd5ef84ff2fedc7d7dd857`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.12.2
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adf9c3fda9d8177b7b23276bf60edc00d93ac48f43a66d894c767b188c47d2`  
		Last Modified: Tue, 03 Dec 2024 02:17:34 GMT  
		Size: 35.8 MB (35760830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe30c2f6b19081578f28d9ccccf35f862d11a58ba4e0065ce828b1455dbd5525`  
		Last Modified: Tue, 03 Dec 2024 02:17:33 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b455ba65587466177bfaf0228adc7008e18828bc059e9e369618c36ade988c56`  
		Last Modified: Tue, 03 Dec 2024 02:17:40 GMT  
		Size: 363.1 MB (363085236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.12.2` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:61dedbbed87e155e745136bc90ab054c50a82878da361446c622b0fbd05f176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62a77b525265f1dc94f38153db3d8c559490f23f3b874b4449e9af3624997a1`

```dockerfile
```

-	Layers:
	-	`sha256:4574fe39846755d947dae849c312c7dfdeacc19bd15e34ef6af5f92f9cbb7892`  
		Last Modified: Tue, 03 Dec 2024 02:17:33 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.13`

```console
$ docker pull rocket.chat@sha256:b8e96805c94724857987136c5819754e730778d783d035658f28b7be99306842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.13` - linux; amd64

```console
$ docker pull rocket.chat@sha256:ee928f74ed7a0792de78551736b0e3112f1c883b4d5e2a4ed6c901679f3c01c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.5 MB (431485110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972a42fd045513f4a40558e9ccc870e918b6e74b88feb38c7aee7cd29af3d862`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.13.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a8cf69b87a528ddb50eb8bff8e36ee2a1b0b8ad964c62608d30293f67c3875`  
		Last Modified: Tue, 03 Dec 2024 02:17:32 GMT  
		Size: 35.8 MB (35760856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f979b3e51392f54a25bbe89884fc49003cf6d67634b9dad2bd4f9423f73c`  
		Last Modified: Tue, 03 Dec 2024 02:17:30 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce6e4558100fa79847207f4d5f20b7514a6a4951e0ebd28c36c8d9e247ebad1`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 365.5 MB (365469853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.13` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:906f0d221ab9c2ab2ca331ff239bfc3ab616f1dfe84e75d6856d63e94055e642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa26b6da4494ba118306e8ef6dbcfe45b22783bcc1e48126b688fa6b77603c`

```dockerfile
```

-	Layers:
	-	`sha256:2de3a922716a6230ad551816817d288ab8d8440485a4fd31a2f7699422f78798`  
		Last Modified: Tue, 03 Dec 2024 02:17:30 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.13.0`

```console
$ docker pull rocket.chat@sha256:b8e96805c94724857987136c5819754e730778d783d035658f28b7be99306842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.13.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:ee928f74ed7a0792de78551736b0e3112f1c883b4d5e2a4ed6c901679f3c01c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.5 MB (431485110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972a42fd045513f4a40558e9ccc870e918b6e74b88feb38c7aee7cd29af3d862`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.13.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a8cf69b87a528ddb50eb8bff8e36ee2a1b0b8ad964c62608d30293f67c3875`  
		Last Modified: Tue, 03 Dec 2024 02:17:32 GMT  
		Size: 35.8 MB (35760856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f979b3e51392f54a25bbe89884fc49003cf6d67634b9dad2bd4f9423f73c`  
		Last Modified: Tue, 03 Dec 2024 02:17:30 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce6e4558100fa79847207f4d5f20b7514a6a4951e0ebd28c36c8d9e247ebad1`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 365.5 MB (365469853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.13.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:906f0d221ab9c2ab2ca331ff239bfc3ab616f1dfe84e75d6856d63e94055e642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa26b6da4494ba118306e8ef6dbcfe45b22783bcc1e48126b688fa6b77603c`

```dockerfile
```

-	Layers:
	-	`sha256:2de3a922716a6230ad551816817d288ab8d8440485a4fd31a2f7699422f78798`  
		Last Modified: Tue, 03 Dec 2024 02:17:30 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.8`

```console
$ docker pull rocket.chat@sha256:8d2396f4426c0e4938b3fd2b8088cdd51230604ea520ba16083661a368e722cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:38ca4b040a0b9a9a9cc77ce7bc2b1e4c96d79bb7287db22f4df68e7e0558214b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381678099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e66df313d9dd0b552566cb5f3c81b586ac2f4e6feec8bcf7bef1edfb32bf194`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.8.7
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26696f1f20d9e3d5752ec9ae52a6aa0ab5e9207d39956ad6d6c3c95b5a27d0f4`  
		Last Modified: Tue, 03 Dec 2024 02:17:20 GMT  
		Size: 35.8 MB (35760859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75eda4b5991af5bd70c7162a05c198a8adcd4da4caf36e7e95a0909a3075078`  
		Last Modified: Tue, 03 Dec 2024 02:17:20 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f708987417fae700f1216422d4e412ee4bb6c4cb8789a2c65bff176663b704a6`  
		Last Modified: Tue, 03 Dec 2024 02:17:26 GMT  
		Size: 315.7 MB (315662836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:8b7e06df670b0a371ded75b6637a75fe61a0490beddb8c5dcdb75f8cbbcbb5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2730ea22769b8e5763e7cda376de9c35f25bea3a57aefa99b5c04aa57d89dce`

```dockerfile
```

-	Layers:
	-	`sha256:e5054fc1d1d54b324ee4f1ede8428a2589227ba53c38a6783e7c48520491ecb7`  
		Last Modified: Tue, 03 Dec 2024 02:17:20 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.8.7`

```console
$ docker pull rocket.chat@sha256:8d2396f4426c0e4938b3fd2b8088cdd51230604ea520ba16083661a368e722cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.8.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:38ca4b040a0b9a9a9cc77ce7bc2b1e4c96d79bb7287db22f4df68e7e0558214b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381678099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e66df313d9dd0b552566cb5f3c81b586ac2f4e6feec8bcf7bef1edfb32bf194`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.8.7
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26696f1f20d9e3d5752ec9ae52a6aa0ab5e9207d39956ad6d6c3c95b5a27d0f4`  
		Last Modified: Tue, 03 Dec 2024 02:17:20 GMT  
		Size: 35.8 MB (35760859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75eda4b5991af5bd70c7162a05c198a8adcd4da4caf36e7e95a0909a3075078`  
		Last Modified: Tue, 03 Dec 2024 02:17:20 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f708987417fae700f1216422d4e412ee4bb6c4cb8789a2c65bff176663b704a6`  
		Last Modified: Tue, 03 Dec 2024 02:17:26 GMT  
		Size: 315.7 MB (315662836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.8.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:8b7e06df670b0a371ded75b6637a75fe61a0490beddb8c5dcdb75f8cbbcbb5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2730ea22769b8e5763e7cda376de9c35f25bea3a57aefa99b5c04aa57d89dce`

```dockerfile
```

-	Layers:
	-	`sha256:e5054fc1d1d54b324ee4f1ede8428a2589227ba53c38a6783e7c48520491ecb7`  
		Last Modified: Tue, 03 Dec 2024 02:17:20 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.9`

```console
$ docker pull rocket.chat@sha256:4daabbe2ecf04a0cc8b6ae8ccae4b5eb81ad85ed73eec67cf3c5d2d6c5c40da6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:28e795a4c7255d98ad8bb009e62e583dc327a84a54a649b0a98de204757a1583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381686514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4affba2b0a00419cc0911519db704ad23106f8b9317ab4f73877cc1219fa431`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.9.7
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ccd28ca0cf46a82f4b85196794d63b126bf251c74f4759513ca9401692ae28`  
		Last Modified: Tue, 03 Dec 2024 02:17:17 GMT  
		Size: 35.8 MB (35760853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b98305b4c1b5b9575664bad5d3b514dad1e5bb9b6dc63599533af51a9ed48d`  
		Last Modified: Tue, 03 Dec 2024 02:17:16 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5410808d11a8788740bb65769172f9a152fab75d335d3c4ed12025fcdeaad9`  
		Last Modified: Tue, 03 Dec 2024 02:17:21 GMT  
		Size: 315.7 MB (315671259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.9` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:2eafb25778caeb49396e7fce01e7b4ad9478af7a53be893c74f88aab702625e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f618c0572cb5e26a0fcb95aa62c3b09d05c05598225304c09a0808939e13df`

```dockerfile
```

-	Layers:
	-	`sha256:2b92bdb211d15ccd8e9baf33b22e4c5d158a85a65c9139f108635e3249459477`  
		Last Modified: Tue, 03 Dec 2024 02:17:16 GMT  
		Size: 21.4 KB (21403 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.9.7`

```console
$ docker pull rocket.chat@sha256:4daabbe2ecf04a0cc8b6ae8ccae4b5eb81ad85ed73eec67cf3c5d2d6c5c40da6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.9.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:28e795a4c7255d98ad8bb009e62e583dc327a84a54a649b0a98de204757a1583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381686514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4affba2b0a00419cc0911519db704ad23106f8b9317ab4f73877cc1219fa431`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=14.21.3
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=6.9.7
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ccd28ca0cf46a82f4b85196794d63b126bf251c74f4759513ca9401692ae28`  
		Last Modified: Tue, 03 Dec 2024 02:17:17 GMT  
		Size: 35.8 MB (35760853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b98305b4c1b5b9575664bad5d3b514dad1e5bb9b6dc63599533af51a9ed48d`  
		Last Modified: Tue, 03 Dec 2024 02:17:16 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5410808d11a8788740bb65769172f9a152fab75d335d3c4ed12025fcdeaad9`  
		Last Modified: Tue, 03 Dec 2024 02:17:21 GMT  
		Size: 315.7 MB (315671259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.9.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:2eafb25778caeb49396e7fce01e7b4ad9478af7a53be893c74f88aab702625e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f618c0572cb5e26a0fcb95aa62c3b09d05c05598225304c09a0808939e13df`

```dockerfile
```

-	Layers:
	-	`sha256:2b92bdb211d15ccd8e9baf33b22e4c5d158a85a65c9139f108635e3249459477`  
		Last Modified: Tue, 03 Dec 2024 02:17:16 GMT  
		Size: 21.4 KB (21403 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7`

```console
$ docker pull rocket.chat@sha256:babf21814d8d4349d1093c1906498bc884ddbae2e43fcc9bcc39cb217595f7af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:f2769b2a813238feaa28b20b8313fc7d76180e2e85b33c1be010bea9ae6ceb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63745ba1d5ee8eab934fe242ff1e42939c75e4cc5aba25266621e361c6bc751`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=20.17.0
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils && rm -rf /var/lib/apt/lists/*   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=7.0.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d85faf8f1b9cd10379fb7e414d69fbd78af15100a3bded6bd5a557b122e46a`  
		Last Modified: Tue, 03 Dec 2024 02:16:40 GMT  
		Size: 48.6 MB (48611354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cbb8cdaac4bc45aa7c75d31c2265de411845ab32ce02d3ff7ba9e2e7b239f5`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6409a7f366a89297b5da546937dda30b8481aa35c7cd6b1851efa8db9f68fcb`  
		Last Modified: Tue, 03 Dec 2024 02:16:44 GMT  
		Size: 327.6 MB (327640146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1b065592303a556802de72b77734870ac4648d35bd946275116a41a797068979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad30b4b9d0d570732292f46d4fc5bf69b6d2ef5ba498814164e26a9d707fbaf8`

```dockerfile
```

-	Layers:
	-	`sha256:3a1959bf2c0f04df58935732a60100dc8fbe38079af521b326b19eee2635750b`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 24.1 KB (24061 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.0`

```console
$ docker pull rocket.chat@sha256:babf21814d8d4349d1093c1906498bc884ddbae2e43fcc9bcc39cb217595f7af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:f2769b2a813238feaa28b20b8313fc7d76180e2e85b33c1be010bea9ae6ceb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63745ba1d5ee8eab934fe242ff1e42939c75e4cc5aba25266621e361c6bc751`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=20.17.0
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils && rm -rf /var/lib/apt/lists/*   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=7.0.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d85faf8f1b9cd10379fb7e414d69fbd78af15100a3bded6bd5a557b122e46a`  
		Last Modified: Tue, 03 Dec 2024 02:16:40 GMT  
		Size: 48.6 MB (48611354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cbb8cdaac4bc45aa7c75d31c2265de411845ab32ce02d3ff7ba9e2e7b239f5`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6409a7f366a89297b5da546937dda30b8481aa35c7cd6b1851efa8db9f68fcb`  
		Last Modified: Tue, 03 Dec 2024 02:16:44 GMT  
		Size: 327.6 MB (327640146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1b065592303a556802de72b77734870ac4648d35bd946275116a41a797068979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad30b4b9d0d570732292f46d4fc5bf69b6d2ef5ba498814164e26a9d707fbaf8`

```dockerfile
```

-	Layers:
	-	`sha256:3a1959bf2c0f04df58935732a60100dc8fbe38079af521b326b19eee2635750b`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 24.1 KB (24061 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.0.0`

```console
$ docker pull rocket.chat@sha256:babf21814d8d4349d1093c1906498bc884ddbae2e43fcc9bcc39cb217595f7af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.0.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:f2769b2a813238feaa28b20b8313fc7d76180e2e85b33c1be010bea9ae6ceb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63745ba1d5ee8eab934fe242ff1e42939c75e4cc5aba25266621e361c6bc751`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=20.17.0
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils && rm -rf /var/lib/apt/lists/*   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=7.0.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d85faf8f1b9cd10379fb7e414d69fbd78af15100a3bded6bd5a557b122e46a`  
		Last Modified: Tue, 03 Dec 2024 02:16:40 GMT  
		Size: 48.6 MB (48611354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cbb8cdaac4bc45aa7c75d31c2265de411845ab32ce02d3ff7ba9e2e7b239f5`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6409a7f366a89297b5da546937dda30b8481aa35c7cd6b1851efa8db9f68fcb`  
		Last Modified: Tue, 03 Dec 2024 02:16:44 GMT  
		Size: 327.6 MB (327640146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.0.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1b065592303a556802de72b77734870ac4648d35bd946275116a41a797068979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad30b4b9d0d570732292f46d4fc5bf69b6d2ef5ba498814164e26a9d707fbaf8`

```dockerfile
```

-	Layers:
	-	`sha256:3a1959bf2c0f04df58935732a60100dc8fbe38079af521b326b19eee2635750b`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 24.1 KB (24061 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:babf21814d8d4349d1093c1906498bc884ddbae2e43fcc9bcc39cb217595f7af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:f2769b2a813238feaa28b20b8313fc7d76180e2e85b33c1be010bea9ae6ceb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63745ba1d5ee8eab934fe242ff1e42939c75e4cc5aba25266621e361c6bc751`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 14 Nov 2024 17:27:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_ENV=production
# Thu, 14 Nov 2024 17:27:12 GMT
ENV NODE_VERSION=20.17.0
# Thu, 14 Nov 2024 17:27:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils && rm -rf /var/lib/apt/lists/*   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
VOLUME [/app/uploads]
# Thu, 14 Nov 2024 17:27:12 GMT
ENV RC_VERSION=7.0.0
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app
# Thu, 14 Nov 2024 17:27:12 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 Nov 2024 17:27:12 GMT
USER rocketchat
# Thu, 14 Nov 2024 17:27:12 GMT
WORKDIR /app/bundle
# Thu, 14 Nov 2024 17:27:12 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 14 Nov 2024 17:27:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 Nov 2024 17:27:12 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d85faf8f1b9cd10379fb7e414d69fbd78af15100a3bded6bd5a557b122e46a`  
		Last Modified: Tue, 03 Dec 2024 02:16:40 GMT  
		Size: 48.6 MB (48611354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cbb8cdaac4bc45aa7c75d31c2265de411845ab32ce02d3ff7ba9e2e7b239f5`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6409a7f366a89297b5da546937dda30b8481aa35c7cd6b1851efa8db9f68fcb`  
		Last Modified: Tue, 03 Dec 2024 02:16:44 GMT  
		Size: 327.6 MB (327640146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:latest` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1b065592303a556802de72b77734870ac4648d35bd946275116a41a797068979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad30b4b9d0d570732292f46d4fc5bf69b6d2ef5ba498814164e26a9d707fbaf8`

```dockerfile
```

-	Layers:
	-	`sha256:3a1959bf2c0f04df58935732a60100dc8fbe38079af521b326b19eee2635750b`  
		Last Modified: Tue, 03 Dec 2024 02:16:39 GMT  
		Size: 24.1 KB (24061 bytes)  
		MIME: application/vnd.in-toto+json

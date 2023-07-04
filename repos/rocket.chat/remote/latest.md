## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:82014a724a99408279507c33ab398d41480942a63c6fb921889cadd8d67c4fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:61fbe3532ea8d0b2aee9dd21a1138fc9992da5aa75e6223e9ac159326ab3cfc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313087465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44c75284dd8b9e1cc2788e35cbb35d781f4872390ba9b3dc92a7a0ea8ccac0a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:47 GMT
ADD file:ca4076bfffab8d09636384070ca253570590554cff76a132afaae5cd89b363b5 in / 
# Tue, 04 Jul 2023 01:20:48 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:36:48 GMT
ENV NODE_ENV=production
# Tue, 04 Jul 2023 02:36:48 GMT
ENV NODE_VERSION=14.21.2
# Tue, 04 Jul 2023 02:37:23 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Jul 2023 02:37:23 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Tue, 04 Jul 2023 02:37:23 GMT
VOLUME [/app/uploads]
# Tue, 04 Jul 2023 02:37:24 GMT
ENV RC_VERSION=6.2.0
# Tue, 04 Jul 2023 02:37:24 GMT
WORKDIR /app
# Tue, 04 Jul 2023 02:38:39 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Tue, 04 Jul 2023 02:38:43 GMT
USER rocketchat
# Tue, 04 Jul 2023 02:38:43 GMT
WORKDIR /app/bundle
# Tue, 04 Jul 2023 02:38:43 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Tue, 04 Jul 2023 02:38:43 GMT
EXPOSE 3000
# Tue, 04 Jul 2023 02:38:43 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:90ac1ecaf92c8ae0cb37d29d8cc01b5802612c12edb933c369ad4c586ea94c6c`  
		Last Modified: Tue, 04 Jul 2023 01:26:21 GMT  
		Size: 27.1 MB (27138502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b92e5753a612244a4853b5d3bd6a6873a45c98bafe4a3d8fec987538896ce5`  
		Last Modified: Tue, 04 Jul 2023 02:44:08 GMT  
		Size: 36.5 MB (36530487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3e8da112091f4cba6acd711677dee5f3549aeb634978d7e9880f8c01a3983`  
		Last Modified: Tue, 04 Jul 2023 02:44:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a8225855ccb554cbbb446a5645968776c95cac3860a2f6eba6f41fb5fba53`  
		Last Modified: Tue, 04 Jul 2023 02:44:46 GMT  
		Size: 249.4 MB (249416672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

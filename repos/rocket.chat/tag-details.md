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
$ docker pull rocket.chat@sha256:0a26bb0a3f3a3a6298a798a19b66e2819404d40a85d03ae5ba0995c23411fb31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2ecd1630c640df78a05002e0a71f230242281dda2b9e403d8b62a85b1b49257a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.7 MB (432684260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cec46dabe131b3a6bd247bc60e751c520a772869dfaaaf4a45ea1f10bcf5d3`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076e9c338e6e26c176698129403a75b4bce1af8a394403b8451ac59aa0d474c`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 35.8 MB (35760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5bbf5e6cfce7344118f62ed06e7e0cb5f0d172bad5640f2962bae6bbbf9135`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b70b5b63b7f8b5b11f24466e6bbeed05ebaf84051874af11f3045ae398c33`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 365.5 MB (365470044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:e91271128f85750b8a331f67038407ab7a6c2615f3bc0a1cb27662823c1ebf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f8ea3af556c6b2ec028df74683035f68a138882a5a4d07029241d12b43558`

```dockerfile
```

-	Layers:
	-	`sha256:08c9b087cc981b2396566ff1cf1f9083f88b68b6a496f3aff4eea46f52858acd`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.10`

```console
$ docker pull rocket.chat@sha256:b31aacc16abd9ca7910e812db90ed5a6c3a093030d212f016a89e0f904e7b261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:4a7301357550b120aae322a8e1ab2978cffca23856ae9f2e42709af34de1bd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438740639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59184392b1423a98cf1bdaef2248cfc9b87b9bfbf4ca592f498b625edfb54daa`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e318c1708fd41bc5a7147abb1d35cba617e009e395a8bf7f3ccfa1df2161cf`  
		Last Modified: Thu, 14 Nov 2024 21:19:21 GMT  
		Size: 35.8 MB (35760871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b286d3f9480c48fbc8c5afd150d1cb9eec35b43045395328b06c8fb235942b9c`  
		Last Modified: Thu, 14 Nov 2024 21:19:20 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d57b7abbc23f74c64ce216d597f184bd4cf50c92d0fd895caafb26209d5f13`  
		Last Modified: Thu, 14 Nov 2024 21:19:29 GMT  
		Size: 371.5 MB (371526447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.10` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:4758028c57181483eb0d78bc07092b7ae94c90cecea168c7cfe999a8b92da708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8870d42d560dcf7a683bb8408c1ce600895d2089b1c292f3d93596bbf5a1c9`

```dockerfile
```

-	Layers:
	-	`sha256:66b362dcffea9cedd02f07626007e93588c352f8ccfb0946667cc3d19ff8ec47`  
		Last Modified: Thu, 14 Nov 2024 21:19:20 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.10.7`

```console
$ docker pull rocket.chat@sha256:b31aacc16abd9ca7910e812db90ed5a6c3a093030d212f016a89e0f904e7b261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.10.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:4a7301357550b120aae322a8e1ab2978cffca23856ae9f2e42709af34de1bd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438740639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59184392b1423a98cf1bdaef2248cfc9b87b9bfbf4ca592f498b625edfb54daa`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e318c1708fd41bc5a7147abb1d35cba617e009e395a8bf7f3ccfa1df2161cf`  
		Last Modified: Thu, 14 Nov 2024 21:19:21 GMT  
		Size: 35.8 MB (35760871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b286d3f9480c48fbc8c5afd150d1cb9eec35b43045395328b06c8fb235942b9c`  
		Last Modified: Thu, 14 Nov 2024 21:19:20 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d57b7abbc23f74c64ce216d597f184bd4cf50c92d0fd895caafb26209d5f13`  
		Last Modified: Thu, 14 Nov 2024 21:19:29 GMT  
		Size: 371.5 MB (371526447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.10.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:4758028c57181483eb0d78bc07092b7ae94c90cecea168c7cfe999a8b92da708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8870d42d560dcf7a683bb8408c1ce600895d2089b1c292f3d93596bbf5a1c9`

```dockerfile
```

-	Layers:
	-	`sha256:66b362dcffea9cedd02f07626007e93588c352f8ccfb0946667cc3d19ff8ec47`  
		Last Modified: Thu, 14 Nov 2024 21:19:20 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.11`

```console
$ docker pull rocket.chat@sha256:2304c5820dc30ad5985b39f4caeef8cf1d4e5a3d72e185e2cdbc6f1d0fd90263
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.11` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a65a527dc59d79ddf3005f58360e616c669295bb4901f726e21b9037cd2b1ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.3 MB (439312142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9878d88edf6203994fd24322369b46acef8429ba948636457e83e23b3b15754a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b12c67ae1885f1855c7a0c092fca5fc85e083149f29e2977b8ba30e5eef9def`  
		Last Modified: Thu, 14 Nov 2024 21:18:30 GMT  
		Size: 35.8 MB (35760879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c525272b32f13d3774f1f10aa6f83fddb9636d59f4aad72cfa9769def458363`  
		Last Modified: Thu, 14 Nov 2024 21:18:30 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c861f2cb463eccbe983cd485828fea2d3068540a85629a0a173d74d2ef1f20`  
		Last Modified: Thu, 14 Nov 2024 21:18:37 GMT  
		Size: 372.1 MB (372097945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.11` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:81a0f3cddee3a999639336374fea4b411b9e83a938dfc71092d48153c6e35002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721ea6ce3193b7b759fbb7fb74efb687d88768621e75c53fe51c647ad697e59a`

```dockerfile
```

-	Layers:
	-	`sha256:bf071e458a5dd010286a49158578fb1c1114d82f7e23e4cb722b38602aabdfa3`  
		Last Modified: Thu, 14 Nov 2024 21:18:30 GMT  
		Size: 21.4 KB (21410 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.11.3`

```console
$ docker pull rocket.chat@sha256:2304c5820dc30ad5985b39f4caeef8cf1d4e5a3d72e185e2cdbc6f1d0fd90263
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.11.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a65a527dc59d79ddf3005f58360e616c669295bb4901f726e21b9037cd2b1ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.3 MB (439312142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9878d88edf6203994fd24322369b46acef8429ba948636457e83e23b3b15754a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b12c67ae1885f1855c7a0c092fca5fc85e083149f29e2977b8ba30e5eef9def`  
		Last Modified: Thu, 14 Nov 2024 21:18:30 GMT  
		Size: 35.8 MB (35760879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c525272b32f13d3774f1f10aa6f83fddb9636d59f4aad72cfa9769def458363`  
		Last Modified: Thu, 14 Nov 2024 21:18:30 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c861f2cb463eccbe983cd485828fea2d3068540a85629a0a173d74d2ef1f20`  
		Last Modified: Thu, 14 Nov 2024 21:18:37 GMT  
		Size: 372.1 MB (372097945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.11.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:81a0f3cddee3a999639336374fea4b411b9e83a938dfc71092d48153c6e35002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721ea6ce3193b7b759fbb7fb74efb687d88768621e75c53fe51c647ad697e59a`

```dockerfile
```

-	Layers:
	-	`sha256:bf071e458a5dd010286a49158578fb1c1114d82f7e23e4cb722b38602aabdfa3`  
		Last Modified: Thu, 14 Nov 2024 21:18:30 GMT  
		Size: 21.4 KB (21410 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.12`

```console
$ docker pull rocket.chat@sha256:a8b30b21abf4447ae290a33c8607923f9af62e223e44d78af2bdb41ff25befbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3992155151f5fe91be9cd9e8a5521c42f47887eeaf1fe551cfc1600757e4c5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.3 MB (430299333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39356c2f9ea9b1728cec32248f5b4d6170d777c5ba56b6bb1c9a2e63ce3cd7a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d7079c57c21fd1f78dbc63ac1647826451b9c0404b7c8e0189c50edb9f68c`  
		Last Modified: Thu, 14 Nov 2024 21:18:06 GMT  
		Size: 35.8 MB (35760853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3895f3e6cc195d4c2455eea7eba177eb34c95cd27969e8ac252b383e3ffcc6`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c522cef3f9b3e57e07c82a30cb2547cab3645b982f215b934eda8a45a6ac7b`  
		Last Modified: Thu, 14 Nov 2024 21:18:10 GMT  
		Size: 363.1 MB (363085158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.12` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:df39b86580efb87d77330395f947464b7abcc57228c9566b7c10afd355c66b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef57ea6adfde4b5ca9dd643ff136374a6f2e9722e7bb604c5668e1cca8d70eb`

```dockerfile
```

-	Layers:
	-	`sha256:c3c3dedd89fcddbe91f603a8f8a8972bb7346bc781736b599eee9d8ab064312f`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.12.2`

```console
$ docker pull rocket.chat@sha256:a8b30b21abf4447ae290a33c8607923f9af62e223e44d78af2bdb41ff25befbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.12.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3992155151f5fe91be9cd9e8a5521c42f47887eeaf1fe551cfc1600757e4c5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.3 MB (430299333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39356c2f9ea9b1728cec32248f5b4d6170d777c5ba56b6bb1c9a2e63ce3cd7a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d7079c57c21fd1f78dbc63ac1647826451b9c0404b7c8e0189c50edb9f68c`  
		Last Modified: Thu, 14 Nov 2024 21:18:06 GMT  
		Size: 35.8 MB (35760853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3895f3e6cc195d4c2455eea7eba177eb34c95cd27969e8ac252b383e3ffcc6`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c522cef3f9b3e57e07c82a30cb2547cab3645b982f215b934eda8a45a6ac7b`  
		Last Modified: Thu, 14 Nov 2024 21:18:10 GMT  
		Size: 363.1 MB (363085158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.12.2` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:df39b86580efb87d77330395f947464b7abcc57228c9566b7c10afd355c66b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef57ea6adfde4b5ca9dd643ff136374a6f2e9722e7bb604c5668e1cca8d70eb`

```dockerfile
```

-	Layers:
	-	`sha256:c3c3dedd89fcddbe91f603a8f8a8972bb7346bc781736b599eee9d8ab064312f`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.13`

```console
$ docker pull rocket.chat@sha256:0a26bb0a3f3a3a6298a798a19b66e2819404d40a85d03ae5ba0995c23411fb31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.13` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2ecd1630c640df78a05002e0a71f230242281dda2b9e403d8b62a85b1b49257a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.7 MB (432684260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cec46dabe131b3a6bd247bc60e751c520a772869dfaaaf4a45ea1f10bcf5d3`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076e9c338e6e26c176698129403a75b4bce1af8a394403b8451ac59aa0d474c`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 35.8 MB (35760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5bbf5e6cfce7344118f62ed06e7e0cb5f0d172bad5640f2962bae6bbbf9135`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b70b5b63b7f8b5b11f24466e6bbeed05ebaf84051874af11f3045ae398c33`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 365.5 MB (365470044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.13` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:e91271128f85750b8a331f67038407ab7a6c2615f3bc0a1cb27662823c1ebf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f8ea3af556c6b2ec028df74683035f68a138882a5a4d07029241d12b43558`

```dockerfile
```

-	Layers:
	-	`sha256:08c9b087cc981b2396566ff1cf1f9083f88b68b6a496f3aff4eea46f52858acd`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.13.0`

```console
$ docker pull rocket.chat@sha256:0a26bb0a3f3a3a6298a798a19b66e2819404d40a85d03ae5ba0995c23411fb31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.13.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2ecd1630c640df78a05002e0a71f230242281dda2b9e403d8b62a85b1b49257a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.7 MB (432684260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cec46dabe131b3a6bd247bc60e751c520a772869dfaaaf4a45ea1f10bcf5d3`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076e9c338e6e26c176698129403a75b4bce1af8a394403b8451ac59aa0d474c`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 35.8 MB (35760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5bbf5e6cfce7344118f62ed06e7e0cb5f0d172bad5640f2962bae6bbbf9135`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b70b5b63b7f8b5b11f24466e6bbeed05ebaf84051874af11f3045ae398c33`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 365.5 MB (365470044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.13.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:e91271128f85750b8a331f67038407ab7a6c2615f3bc0a1cb27662823c1ebf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f8ea3af556c6b2ec028df74683035f68a138882a5a4d07029241d12b43558`

```dockerfile
```

-	Layers:
	-	`sha256:08c9b087cc981b2396566ff1cf1f9083f88b68b6a496f3aff4eea46f52858acd`  
		Last Modified: Thu, 14 Nov 2024 21:17:59 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.8`

```console
$ docker pull rocket.chat@sha256:7163a2898600d4c1341c09078f0989b8ced6db16edd14e3bab9e8ea339dc1ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2d760d607d652ef124271d35aebeea129a8929fb58c6fc3d848572d984502b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382877399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71e79e5289e6096cc4e704d708f15f0a3a0122ffb383b156620d3c016f7334a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b581e6a204bd5c033b06bdfef51dedde9a5fe6b33c6b5a00ed251e211315e1`  
		Last Modified: Thu, 14 Nov 2024 21:18:41 GMT  
		Size: 35.8 MB (35760857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58407486cad4445a5ace0014a084daaa02370bc47f068b7d6c8e1c11093ef5`  
		Last Modified: Thu, 14 Nov 2024 21:18:40 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08c17fcb846ceff3084a67948022f1d667d21179353539dbb2f322658eae5d3`  
		Last Modified: Thu, 14 Nov 2024 21:18:48 GMT  
		Size: 315.7 MB (315663223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:08ca080276de90e9601661b268e26b3bb831d68a8a59bc7438e98c27bdebd715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f2fe6151c3663dca857ca8b0017d7021efa26469c529175072401ce2afd404`

```dockerfile
```

-	Layers:
	-	`sha256:fb1b93970ad260d824fb1388fa313dfb532041175273639b431798bf79343912`  
		Last Modified: Thu, 14 Nov 2024 21:18:40 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.8.7`

```console
$ docker pull rocket.chat@sha256:7163a2898600d4c1341c09078f0989b8ced6db16edd14e3bab9e8ea339dc1ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.8.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2d760d607d652ef124271d35aebeea129a8929fb58c6fc3d848572d984502b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382877399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71e79e5289e6096cc4e704d708f15f0a3a0122ffb383b156620d3c016f7334a`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b581e6a204bd5c033b06bdfef51dedde9a5fe6b33c6b5a00ed251e211315e1`  
		Last Modified: Thu, 14 Nov 2024 21:18:41 GMT  
		Size: 35.8 MB (35760857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58407486cad4445a5ace0014a084daaa02370bc47f068b7d6c8e1c11093ef5`  
		Last Modified: Thu, 14 Nov 2024 21:18:40 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08c17fcb846ceff3084a67948022f1d667d21179353539dbb2f322658eae5d3`  
		Last Modified: Thu, 14 Nov 2024 21:18:48 GMT  
		Size: 315.7 MB (315663223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.8.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:08ca080276de90e9601661b268e26b3bb831d68a8a59bc7438e98c27bdebd715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f2fe6151c3663dca857ca8b0017d7021efa26469c529175072401ce2afd404`

```dockerfile
```

-	Layers:
	-	`sha256:fb1b93970ad260d824fb1388fa313dfb532041175273639b431798bf79343912`  
		Last Modified: Thu, 14 Nov 2024 21:18:40 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.9`

```console
$ docker pull rocket.chat@sha256:c8bbac0499338369c89dfcd4138b75382aa44e938c633203f47de3a8b718c8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:6b216f956460180b2103c4ffb6acf8c9b7c6b9ea7049e84ce9aa1cd133e3e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382885155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987734a06568d50dca23ff5a35ecfead147faacbc5f2081937e0f03cb6f03a85`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e1eae47fa7499c390060b4290821ba3f0d7922a073cf679940a77fd8de83`  
		Last Modified: Thu, 14 Nov 2024 21:17:53 GMT  
		Size: 35.8 MB (35760834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e05b166abc3e5f063efe2ffeee0e64c78f258be8272c59627639104bb36cad`  
		Last Modified: Thu, 14 Nov 2024 21:17:52 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024327183ad5fe1f7b9cbaf486601a91185f0903fbc4fb2b52ac38e7396dcbc2`  
		Last Modified: Thu, 14 Nov 2024 21:18:00 GMT  
		Size: 315.7 MB (315671002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.9` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:619489dd1804d13552c869329de84c4994e5118c5d31dc1c16a007adcef955af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6eec47e0546b3aeadfc9e372cb07dfb17f21e8d0e373ba1811874bb484fa87`

```dockerfile
```

-	Layers:
	-	`sha256:44d23bf53bc8d98646bfb7277aeefdcdfd55183be9ecc43490e37ecd4feed8b5`  
		Last Modified: Thu, 14 Nov 2024 21:17:52 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:6.9.7`

```console
$ docker pull rocket.chat@sha256:c8bbac0499338369c89dfcd4138b75382aa44e938c633203f47de3a8b718c8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:6.9.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:6b216f956460180b2103c4ffb6acf8c9b7c6b9ea7049e84ce9aa1cd133e3e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382885155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987734a06568d50dca23ff5a35ecfead147faacbc5f2081937e0f03cb6f03a85`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e1eae47fa7499c390060b4290821ba3f0d7922a073cf679940a77fd8de83`  
		Last Modified: Thu, 14 Nov 2024 21:17:53 GMT  
		Size: 35.8 MB (35760834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e05b166abc3e5f063efe2ffeee0e64c78f258be8272c59627639104bb36cad`  
		Last Modified: Thu, 14 Nov 2024 21:17:52 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024327183ad5fe1f7b9cbaf486601a91185f0903fbc4fb2b52ac38e7396dcbc2`  
		Last Modified: Thu, 14 Nov 2024 21:18:00 GMT  
		Size: 315.7 MB (315671002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:6.9.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:619489dd1804d13552c869329de84c4994e5118c5d31dc1c16a007adcef955af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6eec47e0546b3aeadfc9e372cb07dfb17f21e8d0e373ba1811874bb484fa87`

```dockerfile
```

-	Layers:
	-	`sha256:44d23bf53bc8d98646bfb7277aeefdcdfd55183be9ecc43490e37ecd4feed8b5`  
		Last Modified: Thu, 14 Nov 2024 21:17:52 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7`

```console
$ docker pull rocket.chat@sha256:385eef8b594902695639408a68442040cd1b40babfebee66be19960442fdb009
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:4b5439c3ecfc209242e8b36d3393fbb9a3bda2a640e31afdef9ff26da4964d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405380026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ef6ff2996ffa18e3730f8309101db49c32772b154f13ba09029d8aa489c942`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ff294b3064001a3d5563bb640dce4821aa6ae20c56d8f7cfdbb085aba0fdc`  
		Last Modified: Thu, 14 Nov 2024 21:51:51 GMT  
		Size: 48.6 MB (48611339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626ef09a826b9d540b6d171ba91458ac2c607b7346011c12d3cb4993b674b0ad`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d6bd18c58a24d5733ad194a0c8045adee372d1f1cc727504fdebeb19cdd918`  
		Last Modified: Thu, 14 Nov 2024 21:51:56 GMT  
		Size: 327.6 MB (327639481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:8214e5dee9aa2eb2a79652ce0f1a036708878ea2c9f63da28b49356e2b0efaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab896382da87125a6ad188d599da940bd435a9f8d339cb04a32be417086b35d`

```dockerfile
```

-	Layers:
	-	`sha256:ff1eb768cbac1bfdf989ed6d2ff432ddc520c7ea28b0c37580078012d06eca2a`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.0`

```console
$ docker pull rocket.chat@sha256:385eef8b594902695639408a68442040cd1b40babfebee66be19960442fdb009
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:4b5439c3ecfc209242e8b36d3393fbb9a3bda2a640e31afdef9ff26da4964d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405380026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ef6ff2996ffa18e3730f8309101db49c32772b154f13ba09029d8aa489c942`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ff294b3064001a3d5563bb640dce4821aa6ae20c56d8f7cfdbb085aba0fdc`  
		Last Modified: Thu, 14 Nov 2024 21:51:51 GMT  
		Size: 48.6 MB (48611339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626ef09a826b9d540b6d171ba91458ac2c607b7346011c12d3cb4993b674b0ad`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d6bd18c58a24d5733ad194a0c8045adee372d1f1cc727504fdebeb19cdd918`  
		Last Modified: Thu, 14 Nov 2024 21:51:56 GMT  
		Size: 327.6 MB (327639481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:8214e5dee9aa2eb2a79652ce0f1a036708878ea2c9f63da28b49356e2b0efaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab896382da87125a6ad188d599da940bd435a9f8d339cb04a32be417086b35d`

```dockerfile
```

-	Layers:
	-	`sha256:ff1eb768cbac1bfdf989ed6d2ff432ddc520c7ea28b0c37580078012d06eca2a`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.0.0`

```console
$ docker pull rocket.chat@sha256:385eef8b594902695639408a68442040cd1b40babfebee66be19960442fdb009
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.0.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:4b5439c3ecfc209242e8b36d3393fbb9a3bda2a640e31afdef9ff26da4964d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405380026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ef6ff2996ffa18e3730f8309101db49c32772b154f13ba09029d8aa489c942`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ff294b3064001a3d5563bb640dce4821aa6ae20c56d8f7cfdbb085aba0fdc`  
		Last Modified: Thu, 14 Nov 2024 21:51:51 GMT  
		Size: 48.6 MB (48611339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626ef09a826b9d540b6d171ba91458ac2c607b7346011c12d3cb4993b674b0ad`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d6bd18c58a24d5733ad194a0c8045adee372d1f1cc727504fdebeb19cdd918`  
		Last Modified: Thu, 14 Nov 2024 21:51:56 GMT  
		Size: 327.6 MB (327639481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.0.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:8214e5dee9aa2eb2a79652ce0f1a036708878ea2c9f63da28b49356e2b0efaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab896382da87125a6ad188d599da940bd435a9f8d339cb04a32be417086b35d`

```dockerfile
```

-	Layers:
	-	`sha256:ff1eb768cbac1bfdf989ed6d2ff432ddc520c7ea28b0c37580078012d06eca2a`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:385eef8b594902695639408a68442040cd1b40babfebee66be19960442fdb009
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:4b5439c3ecfc209242e8b36d3393fbb9a3bda2a640e31afdef9ff26da4964d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405380026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ef6ff2996ffa18e3730f8309101db49c32772b154f13ba09029d8aa489c942`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ff294b3064001a3d5563bb640dce4821aa6ae20c56d8f7cfdbb085aba0fdc`  
		Last Modified: Thu, 14 Nov 2024 21:51:51 GMT  
		Size: 48.6 MB (48611339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626ef09a826b9d540b6d171ba91458ac2c607b7346011c12d3cb4993b674b0ad`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d6bd18c58a24d5733ad194a0c8045adee372d1f1cc727504fdebeb19cdd918`  
		Last Modified: Thu, 14 Nov 2024 21:51:56 GMT  
		Size: 327.6 MB (327639481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:latest` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:8214e5dee9aa2eb2a79652ce0f1a036708878ea2c9f63da28b49356e2b0efaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab896382da87125a6ad188d599da940bd435a9f8d339cb04a32be417086b35d`

```dockerfile
```

-	Layers:
	-	`sha256:ff1eb768cbac1bfdf989ed6d2ff432ddc520c7ea28b0c37580078012d06eca2a`  
		Last Modified: Thu, 14 Nov 2024 21:51:50 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json

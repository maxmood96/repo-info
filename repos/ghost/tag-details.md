<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.23`](#ghost6-alpine323)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.45`](#ghost645)
-	[`ghost:6.45-alpine`](#ghost645-alpine)
-	[`ghost:6.45-alpine3.23`](#ghost645-alpine323)
-	[`ghost:6.45-bookworm`](#ghost645-bookworm)
-	[`ghost:6.45.0`](#ghost6450)
-	[`ghost:6.45.0-alpine`](#ghost6450-alpine)
-	[`ghost:6.45.0-alpine3.23`](#ghost6450-alpine323)
-	[`ghost:6.45.0-bookworm`](#ghost6450-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.23`](#ghostalpine323)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:6`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6.45` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45-alpine`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.45-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45-alpine3.23`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.45-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45-bookworm`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6.45-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45.0`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6.45.0` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45.0-alpine`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.45.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45.0-alpine3.23`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.45.0-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.45.0-bookworm`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6.45.0-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.45.0-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.45.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:2c7f6bbeef2edc304d17a45f3ac3d8df154af7d69fda20951721080b16611fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5a5355d5726c7fc2eb095c6eadedfca8618e7af260eb27182394b568237fc478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235370762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617615bf2e3e5b13197d73a5c0e107679675d58d86151aa10ca9a81430206b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 13:45:41 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:44 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:11:50 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:11:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:11:52 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:11:52 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:24 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:24 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d807ec34022e58b147170ed06ac6574e10f748a9f1d17a6e9eeed62893fb`  
		Last Modified: Thu, 18 Jun 2026 13:46:00 GMT  
		Size: 52.3 MB (52313653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b64a434a6049cc64987a99449162bd83b66f9b6c3631c6556b8cb2880ebe3`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 1.3 MB (1262093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d493f9328c66389ed1f4f2ea9ee2690f8cced9616145d1d5a59771ceb3a2a0`  
		Last Modified: Thu, 18 Jun 2026 13:45:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83658ee415883d8accf0d8223b9fb5fd5184794bed842b2ddf9f6f07f020b95e`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130a0e766d28eeef23a554ecc0d22d86eeb2060f72800aeddc29dedce3325a0`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 925.1 KB (925092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a635664d0ddf9da6e0127b54cf26d4d6f6866072d1258611e6018bdcaef2d`  
		Last Modified: Thu, 18 Jun 2026 14:13:06 GMT  
		Size: 14.6 MB (14565854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80f2e1032d422a93dc548e6f51316e1699e43eee121f36fb5c2e59e04b790b`  
		Last Modified: Thu, 18 Jun 2026 14:13:09 GMT  
		Size: 161.6 MB (161617008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e0fcab08736f7445544f75a16fd4717019ca592c4b5f3e4e82c95ea0ad00c`  
		Last Modified: Thu, 18 Jun 2026 14:13:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:01aca7a83cd1d00ce0a052f1b3152e7d2fd17039f54ee3b4741c212b976cb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62713923d4629b185ff1e9a8307985adc22961a57be48e61d208e848b371dcf3`

```dockerfile
```

-	Layers:
	-	`sha256:c2307e6887ce8932f709fd096a26d904c00920d20617193814ae6c7812b5d520`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 3.3 MB (3328254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e849ac15916a344177a609232cd2303240464a2f176ddabc635c45fbdaad3461`  
		Last Modified: Thu, 18 Jun 2026 14:13:05 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b11a57f48176baa88ceedd5542347a1c5898560f89e22908222337923356971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236195605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac93956745339d754724207275b165b028d2df80353f96a74770f202794625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 14:18:16 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 14:18:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="0157386028056147668de74f5ba83a5834f695661580890c49b963ffd370be34" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:16 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 14:18:20 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:18:20 GMT
CMD ["node"]
# Thu, 18 Jun 2026 15:10:02 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 15:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 15:10:05 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 15:10:05 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 15:10:16 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 15:10:16 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 15:10:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 15:10:41 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 15:10:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:10:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:10:41 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 15:10:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60f12189c6873b5f636b365584b1a933a3e41aa77a7c3bc1551c68700b8ce0`  
		Last Modified: Thu, 18 Jun 2026 14:18:37 GMT  
		Size: 52.7 MB (52666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d645a03f987b698d380630b684d4033b5edf66cbd8e5e046669a8103a1e6d`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 1.3 MB (1262967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f5bf38dfd4c5164ff0629d84c93146cb5957eacbcb001b91b4d39e5664a25`  
		Last Modified: Thu, 18 Jun 2026 14:18:36 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4808e23146b31c6d2cc9674f9958b24848e0bc45ee3adc7edbbbb8c5a18931c`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 891.3 KB (891277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7de345c13eb6ad3c0c7d1170da7948ee17cbe71d3b708431c7eb34c83cfa7d`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 879.2 KB (879177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a93d78c9b62c95fdee5de707386f53c28141ab47b3f9cfc5a0ea9b8c4dc40d`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 14.6 MB (14569512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a1ac05369924391ee12db7eb28e23f0d73cb04164f01fd68a8f4aca877392`  
		Last Modified: Thu, 18 Jun 2026 15:11:30 GMT  
		Size: 161.7 MB (161725180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec49fbd2d79490603c02ac0507d64867de51da486b48f06857ddb3d3ac4f89`  
		Last Modified: Thu, 18 Jun 2026 15:11:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:07fe5482a2285ada62c1a9c611588cdfcc327c6e51626785252ffc827c8ea417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561e64662815b0f84815d07134805a7be27f925887297469a0c66a52f6bd441e`

```dockerfile
```

-	Layers:
	-	`sha256:5198ec4e35e39cb8bf774e80282c448d9d6d0de1c3e6791d81498881e33046f7`  
		Last Modified: Thu, 18 Jun 2026 15:11:27 GMT  
		Size: 3.3 MB (3327738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f8e45d8cdd48ec300bdb94b105a330532f981012ccc7a3af2e50ef6da202a0`  
		Last Modified: Thu, 18 Jun 2026 15:11:26 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:9134d89731b7be99f672077d2a3d4190a1985eaf82c65a5ccf2b9e338b5471d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:73912ce576b774a24302eccf6d62a8daa29df79d0e7aa175095d46e463fc4a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257643386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46f4ee0afa95d43c113df0fc80c6c1ac66c18c21ad9b3a1784000eb0472ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:21 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:21 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:12:02 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:12:02 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:12:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:12:10 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:12:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:12:42 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:12:42 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:12:42 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3790d1cc1668bbb96061c9842c9b08637fd0fe865e0fba75a876d9c6f39a74`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f9c72f6056cb05411975a19395822d67c1ad0be17b7099144ff827e2696ff`  
		Last Modified: Thu, 18 Jun 2026 13:46:35 GMT  
		Size: 49.9 MB (49929635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89dda362aaa910fe0f00f1359e9c7d75a4daa1996a0c0be6b3dc8fe1b55258`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc9ed683951fde1a681129a1f0d99c253586800606e93cf8c4846c9c0dad45`  
		Last Modified: Thu, 18 Jun 2026 13:46:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd7a5cab37baca8fdfeba7b6841e05386d15e72a1e4a3cd85d5badf4ceced5`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 1.2 MB (1247550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca817a414f183a40f9ef66e7012cba3d4d4f5c5b4a2dbfaf60c370d1c3181620`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 14.6 MB (14566426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768ec303680d2b972b989a00ca3fcf564c77b23ab36277e0dbb232546f87fdf`  
		Last Modified: Thu, 18 Jun 2026 14:13:24 GMT  
		Size: 161.9 MB (161945161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240569a44e6fc8ff47e21aa76e44f5d2c6117b9ecf47e04442fb59c195e8047`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:6231cff74053bd4e23da1853bd34f9d8a15031444a5965b20e8d4bbbe447327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836bdbb945609dfa68b1b0eaee57509a57e92e9354834078e77d568fcbac9e0`

```dockerfile
```

-	Layers:
	-	`sha256:5df33c3a1cac74643c2cac2046d0fe9dcefec6a8a6110589934e057889e542bc`  
		Last Modified: Thu, 18 Jun 2026 14:13:21 GMT  
		Size: 5.5 MB (5540233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247c0ce944a35ccde86143a6fc5d0568044b0950cfb4370a835e478c0dded463`  
		Last Modified: Thu, 18 Jun 2026 14:13:20 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:88fe9f49e3530e571d20617742fc2eb3fa97ef9001de164844c4f34b52f62d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262635388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac3aaa348530ab72ba7b040612d40af15eaded16ff0a4c67691ee1c6b7632b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:45:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:45:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:38 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:45:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:45:51 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:19:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:19:59 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:19:59 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:20:12 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:20:12 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:22:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:22:19 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:22:19 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:22:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5562898275efc5b5f73ca0355ee2da222ab1ccd4aaec83894264bed85f1c8f`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc59969586b371adf2e0559f340b2d86d2cc1effa5844d6c44946ea661e5a8`  
		Last Modified: Thu, 18 Jun 2026 13:46:06 GMT  
		Size: 44.6 MB (44627937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6079d55179d57a67f26a3599e1e259ce10e52bbb79f10bc4ec9a4bab300da2c`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 1.7 MB (1712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6d3bf40b78cd23b5c0ece29e3fbed93a51b29b3d23de1b4ce32f5cae07bf`  
		Last Modified: Thu, 18 Jun 2026 13:46:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7be86798ed9c119095fa78f3bc618742c38176e989755f0579476a40f8bcc`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 1.2 MB (1214364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c73c4f1258a16cb997585377eaf98dd962e5722949ecabed4c4a375c80efe8`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 14.6 MB (14560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04fb0a01afd7b94cf4533e2eb125bc488752002ab52449167315bdb867dfed`  
		Last Modified: Thu, 18 Jun 2026 14:23:12 GMT  
		Size: 176.6 MB (176571320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905bcb8e9ff32a7a3fa7fe344682f0ab55e25ddc9bb3defd1ce82dbd8524cee`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:3d7902805ac366cb78c3195235682eefa8ff95e1cd644c31ce8d8d5676b9eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa24387253abc086449a387f8eccc41f8ac1055fe584782c1b3bf1a1e905b7e6`

```dockerfile
```

-	Layers:
	-	`sha256:0cbf4f8956167ca1f106902f442c9fb5e4648fbcd3b16c15c0ffe465e2b90e3f`  
		Last Modified: Thu, 18 Jun 2026 14:23:08 GMT  
		Size: 5.5 MB (5546059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebab228347e7013c29dc3e5cd1033724e39cd2e3a0f058ce245923283d87f44d`  
		Last Modified: Thu, 18 Jun 2026 14:23:07 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:07cb1a545ac5539b569a8943578e89cd359c35938404fb38225c3b707df21021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257657075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878fe5a64e9f7ce82c6d73c2b3c4214f6a3138741f83854571849e274afb77e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 13:44:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 13:46:30 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:30 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 13:46:41 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 13:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 13:46:41 GMT
CMD ["node"]
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 14:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 14:36:49 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 14:36:49 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 14:37:00 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 14:37:00 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 14:37:37 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 14:37:38 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 14:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 14:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 14:37:38 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 14:37:38 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f906db70a3f1126c33d13a412f185f96ff59cfb8bb101d7c7fa34b75719524`  
		Last Modified: Thu, 18 Jun 2026 13:45:02 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300eb2289cc5d6698d2ea5cfb1a14108e6f39ddb987122da62df33d412ca0d`  
		Last Modified: Thu, 18 Jun 2026 13:46:57 GMT  
		Size: 50.1 MB (50062240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fdb9e0f82d626598eda8d6ea561fc1869b02191f3ff5b912a409ffd3dce92`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 1.7 MB (1712608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b178ee0457ab784e357d588266a7d516730ff89ecde46d598069a46c2a32f1f`  
		Last Modified: Thu, 18 Jun 2026 13:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb627193cd53040e88a40e5505afb250fe3c15e561d8bd3d00d340d2c45f6f`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 1.2 MB (1201447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f140458888bf38a562df195a24f5ed7ccf2f7e51125506dadb94249c13119`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 14.6 MB (14567757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0a9f65f45ba51d4106436a216896e9b2c54d0d691eb37174882e49ed5150`  
		Last Modified: Thu, 18 Jun 2026 14:38:30 GMT  
		Size: 162.0 MB (161986380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7815cfb9ca8c76904762c4a40417cf11ee904c2ca105952c1b11ee63a4d5d5`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:dc14e3844957b63942aefced2f1612f82b31318d966d850afeb88a5b5e8c0a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3143c764d077ce751592a2ba4c9cb8aa346d8837def30256436c121f2063ad`

```dockerfile
```

-	Layers:
	-	`sha256:c82d1553184d6516956a5873829aafcd04e1cdae5d3b509ab91771e2eef45bfd`  
		Last Modified: Thu, 18 Jun 2026 14:38:26 GMT  
		Size: 5.5 MB (5540562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd46217b478e6d298b78f4fc44c9d557b37b1fcd4c116a57801c46a60136620`  
		Last Modified: Thu, 18 Jun 2026 14:38:25 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:24cbf57c65fe59012147ae641abd8118dc703a2dce8684b385f854c29b284125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273613347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc88a7a4b4ce61e296baa53e31f8d988a458dae7c7b66d075aa8f8254ef700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 18 Jun 2026 15:17:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV NODE_VERSION=22.23.0
# Thu, 18 Jun 2026 15:17:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:17:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jun 2026 15:18:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 15:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 15:18:01 GMT
CMD ["node"]
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Jun 2026 16:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 16:09:09 GMT
ENV NODE_ENV=production
# Thu, 18 Jun 2026 16:09:09 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 18 Jun 2026 16:09:21 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Jun 2026 16:09:21 GMT
ENV GHOST_VERSION=6.45.0
# Thu, 18 Jun 2026 16:11:22 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Jun 2026 16:11:23 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Jun 2026 16:11:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 16:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 16:11:23 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Jun 2026 16:11:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8b87904bcf5bb664bf18cfe843f828c708461257e34035b1a3a75c29d4966`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b18e6ef99cf42026c3738ed4283793a3745b6356f4ece8c3aa3e8055fcc4d`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 50.1 MB (50088257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e2ca4a080a3b760378b7370cb879b20ff2010724a15e03ecdac57428b0b94`  
		Last Modified: Thu, 18 Jun 2026 15:18:28 GMT  
		Size: 1.7 MB (1712665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801981871ed8796173fb760578ebc8d8d0938b669e141f9fabadf0e4e028511c`  
		Last Modified: Thu, 18 Jun 2026 15:18:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce82ddf8d52731c90dcf8bbb6899a0997374256543c97fe8eb83914b36697`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfcafa1d5f935399f5acf901e08bb40f6d6178e34f541a2d7663172aa890b9`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 14.6 MB (14575252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0013708bae2f76822f99ee4456c2fbcbf7317533a728ece82464ee6689e98d`  
		Last Modified: Thu, 18 Jun 2026 16:12:40 GMT  
		Size: 179.1 MB (179117950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5792dc974d79af42bd6f860c4bf79e7f01981e003d42fd16366ebdac0be4c4fd`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:8b8a8d2f5d9d23ff1ccfa163f8c3306ed239461315c8954b5246af2b12a05ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769586d1c6ddddf89da37449b4dc9b1636302ab38eddd4b18ccd7f3324b310`

```dockerfile
```

-	Layers:
	-	`sha256:e142381ccc8ef91658826054402ab66bbe75eaf748b6adf4f7df7d791cdb2bea`  
		Last Modified: Thu, 18 Jun 2026 16:12:37 GMT  
		Size: 5.5 MB (5537091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae856e71fc56fbfe603cbb7f493c01867d50e9ec3719499049ea738b71ed526e`  
		Last Modified: Thu, 18 Jun 2026 16:12:36 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

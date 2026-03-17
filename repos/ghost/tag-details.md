<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.23`](#ghost6-alpine323)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.22`](#ghost622)
-	[`ghost:6.22-alpine`](#ghost622-alpine)
-	[`ghost:6.22-alpine3.23`](#ghost622-alpine323)
-	[`ghost:6.22-bookworm`](#ghost622-bookworm)
-	[`ghost:6.22.0`](#ghost6220)
-	[`ghost:6.22.0-alpine`](#ghost6220-alpine)
-	[`ghost:6.22.0-alpine3.23`](#ghost6220-alpine323)
-	[`ghost:6.22.0-bookworm`](#ghost6220-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.23`](#ghostalpine323)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:6`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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

### `ghost:6.22` - linux; amd64

```console
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22-alpine`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22-alpine3.23`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22-bookworm`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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

### `ghost:6.22-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.0`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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

### `ghost:6.22.0` - linux; amd64

```console
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.0-alpine`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.0-alpine3.23`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22.0-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.0-bookworm`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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

### `ghost:6.22.0-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.0-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:ac533a6988ee282273c26f3752ed8b61dc34a804571e14a2de60fe0dabbd1aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:1d9e252815cafd114f923a4c524e22bc00b8db8ead351caf865334e840ea11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220753189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1717b33b94739d0ad8f1b4bd0fc9be3750bc4d075c3b4df83a5866fcbe96fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:47:30 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:47:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:47:32 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:47:32 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:45 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:55 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:55 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bf72576ccb837828771f09a5635edcd183fcc5c180185f16a2a0032d57bf16`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4c676ffcab978b313f69aa85b279c3a517a08c722eb2ef4124ddab662c1b0`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 928.3 KB (928319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65bcb1c2d6e14bdaf45eb2c233e75ba34c0acd1d9589402a29e7b70f24fb650`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 12.1 MB (12143646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ad9fda77a3cf5815abf6092ced79da9805f2d19a197d44f12d08aefbdead5`  
		Last Modified: Fri, 13 Mar 2026 23:50:37 GMT  
		Size: 149.7 MB (149662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cdea77158e56d2b59d1c5dc37bd1e8ea386be1e7587b64b1f3d32c3c1e1e8`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1e8e48d9066b96e3785c77616896731ffc10c9b03a2c86a6c57ac328327c0937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef29ee49c5de9610e41ffdaee6ea29c562a59fc59f0ffc5ef8225967cfa17`

```dockerfile
```

-	Layers:
	-	`sha256:702d50d1d7c251c85c919614e44b74559868010dc2fd51588256f934528a77bc`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 3.7 MB (3683885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c1b2c4e814930eb3345b7c63d35e36e5237834ef0fb51fc6b672ce627841c`  
		Last Modified: Fri, 13 Mar 2026 23:50:33 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a55b2460f498068a6902fd7d7e3b90de5179f6656039aff1dee6f6f2de8d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232600207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190655c77f3d4284c443d0423c7b9d447c9671e3bb904d8d23e33fe50fd58d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Fri, 13 Mar 2026 23:46:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:46:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:46:47 GMT
ENV NODE_ENV=production
# Fri, 13 Mar 2026 23:46:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 13 Mar 2026 23:47:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 13 Mar 2026 23:47:01 GMT
ENV GHOST_VERSION=6.22.0
# Fri, 13 Mar 2026 23:49:50 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
WORKDIR /var/lib/ghost
# Fri, 13 Mar 2026 23:49:50 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 13 Mar 2026 23:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:49:50 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 13 Mar 2026 23:49:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de2f4848813b8dedd1b07ccab11799ae0f32a7d8d5d4bab5e1a774332b6167`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 891.3 KB (891307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f502efb34661691e68c0abcf26da91559cf67f95843be4166b552732f3c8912`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 881.3 KB (881275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f709d350f23efba37ab19d36c7b438d13e9916aee11cf0907e1cb54194b0cc1`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 12.1 MB (12146632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2776aca7376a09583b87e5e62d2b086b98bec49ca968e7d4c028c6d9601c2`  
		Last Modified: Fri, 13 Mar 2026 23:50:38 GMT  
		Size: 160.5 MB (160523123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3e3aaa83ca219d7e6e42e06e040cb384874d8886cc501b6fcf63d6329963f`  
		Last Modified: Fri, 13 Mar 2026 23:50:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:b0cac520425bc40b94267cbfdb9f6d552ae0787982b9f0d05fe2c3ba881db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58787226cc204fb7e5fd965f4fc3fd275b8e61fd1ecd8a006cc126e3db19af22`

```dockerfile
```

-	Layers:
	-	`sha256:0be3761a71ba88e5656aa96b8be4e319ab736c3ea9ca92c3d0599030cdb07aa6`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 3.7 MB (3683391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eb76de108dafc6ce6add879065141f950f02098531e39ae1cde7100d97dfcf`  
		Last Modified: Fri, 13 Mar 2026 23:50:34 GMT  
		Size: 26.6 KB (26581 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:2c49abdadaf4ac2eb86319ae1304c8415ffaf54ce12083e2674577dfbcaaaca4
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
$ docker pull ghost@sha256:bd684df31ac3ee4763fa94fdacf431eaaff0f7c51cc35adec880f1d26eea5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243129561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f360b4aaafcdb96c4b193c5ff4a23278afde2b5fec151b8974027601ac85eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:41:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:41:58 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:41:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:42:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:42:11 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:44:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:44:28 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:28 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:44:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d7096e51d5526d4e7575d26ece069688ad6342a213dae5fb5d43f642ec23c`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 1.2 MB (1247546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602b0a0d2e5778d85854d47fb2b70bbb3c29e537709b3f04c9786033b258667`  
		Last Modified: Mon, 16 Mar 2026 23:45:08 GMT  
		Size: 12.1 MB (12141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4fea63ff8ea34317976a0b1b7e28bb3b28c5c82e6a392ceee19a8e6d00dd3b`  
		Last Modified: Mon, 16 Mar 2026 23:45:10 GMT  
		Size: 149.8 MB (149837508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f8a49ccf7a157e73a6961f992be9255c3314e6e5fd95cd7f26debb9f60e93`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:0986c47792913e9a6001617a8fb352b4174a33c47f985b18b01af9ace1f86927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c590f336654f3b8605dcec5884f2354f5fcaf5f6bf057944e2680ea727a07`

```dockerfile
```

-	Layers:
	-	`sha256:1bfed8071978d139e4fa8bf201f6ab6b260ba6e8cbb14fa4d8b72cad5710827d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 5.9 MB (5895886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85856dc21973ae22e846b38db4347dad8c24eeac39ecf69d765443376c4a47d`  
		Last Modified: Mon, 16 Mar 2026 23:45:07 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:019ca06430efc77c9bff6444c765988681ea056aaba187b8a178f19f2dcae048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234580431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa4e8542d5d81e1b86116d3b50ac626e66211d21717f79969b8868576791696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:07:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:07:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 01:07:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 01:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 01:08:05 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 01:11:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 01:11:10 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 01:11:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:10 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 01:11:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3199d33318a0c62e808ea60516ed434607acf3d92b2a5b4787572cdd551a5f`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 1.2 MB (1214366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0e499edcdb24c59ac9cceed031a40cf36534bae13e8091d4d3ccecbc04c6a3`  
		Last Modified: Tue, 17 Mar 2026 01:11:54 GMT  
		Size: 12.1 MB (12137201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a5361b05340899461401b83b050bc7e968a86d7c04fdddc4c11b7f8b13036`  
		Last Modified: Tue, 17 Mar 2026 01:12:01 GMT  
		Size: 150.9 MB (150896641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ac5eb87370bab569a065fc099291900c3994525d79ebbce39172e500c8352`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:0d2298f63ae0a0a1ae4c124a71d19f01264e263f00b369abebd66b7209c9ead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1567420c946986a8f14950cba28cb45ec9c4b4016d8e489c3335f37c3cb74c4f`

```dockerfile
```

-	Layers:
	-	`sha256:8d26d122c43e409780d4f16ed1a24cfa8be3cc9eaef36912b336ad8dedf244e7`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 5.9 MB (5898683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17285889b9efdc4705fd0c81c5ff6ae5407dffdddaefc0991bf7315d6ca26ea2`  
		Last Modified: Tue, 17 Mar 2026 01:11:53 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:14dedee32ef09c3a9610347590ba8c5e04c6764928627aa6a75111c2ce28c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243192158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930ffb6cb48ba12239539ef464359cfd60770b4f7b86ed65bd5d8d77deb4939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:47:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:47:20 GMT
ENV NODE_ENV=production
# Mon, 16 Mar 2026 23:47:20 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Mon, 16 Mar 2026 23:47:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Mar 2026 23:47:35 GMT
ENV GHOST_VERSION=6.22.0
# Mon, 16 Mar 2026 23:50:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Mar 2026 23:50:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Mar 2026 23:50:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:50:17 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 16 Mar 2026 23:50:17 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63f5531e4cdc636d371211dc698a792bafd75888a8b4dbc8d7881692f577b7`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 1.2 MB (1201504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac40137d9a52eb3e28d76f5467ad830042fb079d0a497de299c2d9eb7410deb`  
		Last Modified: Mon, 16 Mar 2026 23:51:02 GMT  
		Size: 12.1 MB (12145619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f252fba51123f55c35eb6adc5cbf4a1b8bd250ea0b25f230e0ec5b15af1dec`  
		Last Modified: Mon, 16 Mar 2026 23:51:05 GMT  
		Size: 149.9 MB (149927521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400442c1324f34509a21de580d7b9f63efb0d43973bbc4dc6e4f27fdc29d826b`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:eebdbbecb168054b5a86ec02dacbc5bd2bd97fce42496efb30b893ff4f8e9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ec3862fbdc6a07f667571632c8f9c82bbfc50c6a243da76b16cf0a16e9974b`

```dockerfile
```

-	Layers:
	-	`sha256:eedf0f5c586739bbf724f01865acfed837ca045ba49a379853289317bb47552f`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 5.9 MB (5896237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776572a912982978bbb173f0b915984ed45767bd3a510334037fde37a36e2fb3`  
		Last Modified: Mon, 16 Mar 2026 23:51:01 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:eee1495bcd6f1f3536e4c3e554ecfff7799312a1feec63f5477eb8b4b0a79f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245097370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cf208ff37120f7e67ce3e23f76c43af37aa63c88425174205c738d11b2fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:11:49 GMT
ENV NODE_ENV=production
# Tue, 17 Mar 2026 02:11:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 17 Mar 2026 02:12:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 17 Mar 2026 02:12:16 GMT
ENV GHOST_VERSION=6.22.0
# Tue, 17 Mar 2026 02:15:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
WORKDIR /var/lib/ghost
# Tue, 17 Mar 2026 02:15:06 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 17 Mar 2026 02:15:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:15:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:15:06 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 17 Mar 2026 02:15:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ad01e433a2ce4d312954c7419a745a1d164d8949c151f9b64db8edd025325`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 1.2 MB (1221339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21505e541ea3cdcd31503c5db07f6e405701fae622f2876f0f346c6d131ce752`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 12.2 MB (12152589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d8a5c60bfce34a71950e882c5909e9566d1687d33a186bcaca1b94de526153`  
		Last Modified: Tue, 17 Mar 2026 02:16:18 GMT  
		Size: 153.0 MB (152983901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a5dfe82fa97c27c4518b73fb5d41dfb83bf44614c154b3a3e713f99aaa40`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:930a489acb385efbf60a3d13d59f782b81e6b917add1197efab0a40340952b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e8916573965d5869043ec9525624542f1640282783e6ae5254fb8f2fe2486`

```dockerfile
```

-	Layers:
	-	`sha256:f737577ee8742c40c1b18f6456e7941178e6479d954cda4bd573ad513deeebd4`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 5.9 MB (5889711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a97bf43b05b0bd52f1802eed618b381298787c0ed597d685ec4bca60c7f20c6`  
		Last Modified: Tue, 17 Mar 2026 02:16:15 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

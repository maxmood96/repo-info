<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.23`](#ghost6-alpine323)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.38`](#ghost638)
-	[`ghost:6.38-alpine`](#ghost638-alpine)
-	[`ghost:6.38-alpine3.23`](#ghost638-alpine323)
-	[`ghost:6.38-bookworm`](#ghost638-bookworm)
-	[`ghost:6.38.0`](#ghost6380)
-	[`ghost:6.38.0-alpine`](#ghost6380-alpine)
-	[`ghost:6.38.0-alpine3.23`](#ghost6380-alpine323)
-	[`ghost:6.38.0-bookworm`](#ghost6380-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.23`](#ghostalpine323)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:6`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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

### `ghost:6.38` - linux; amd64

```console
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38-alpine`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.38-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38-alpine3.23`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.38-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38-bookworm`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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

### `ghost:6.38-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38.0`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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

### `ghost:6.38.0` - linux; amd64

```console
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38.0-alpine`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.38.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38.0-alpine3.23`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.38.0-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.38.0-bookworm`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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

### `ghost:6.38.0-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.38.0-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.38.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:ae833b67204708c9d153afba228eaa4d30d71208d2c2304d5a56f5d855e06344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:ad41734600c066d3ae5f6d41dfeb2eee92e9ce0b61f9063ae7f085982cea29b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317080560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa6cbc6304058ef4216c97dc4c5efc2728150e3a9cd4f3de1a665ef20ea187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:40 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 20:46:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 20:46:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:46:43 GMT
CMD ["node"]
# Wed, 13 May 2026 18:17:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:18:02 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:18:02 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:18:10 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:18:10 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:18:40 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:18:40 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:18:40 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:18:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e177ba73d9ff6d235c7d32bf216469630dcce0a52a6cbde08bd868b7a07e7d5`  
		Last Modified: Wed, 15 Apr 2026 20:46:58 GMT  
		Size: 52.0 MB (51962079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc15311d45b63612aec3e37d607941ddc636bd3ab45235d8391dc5b2b90faf4`  
		Last Modified: Wed, 15 Apr 2026 20:46:56 GMT  
		Size: 1.3 MB (1262123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa0019f928dcee6004de6c4b85d75774f993212504ac816ede0f3c6ae097de`  
		Last Modified: Wed, 15 Apr 2026 20:46:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a964d94a327b32b74644d71c2625a5468c2041453b834dbb341b83a585de2b`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 821.9 KB (821892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d47ad86cba04029cf84f38df486ab6a6bfb3c28c3d39a5e86222a9ffc889e`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 925.1 KB (925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52071576659f72adb1b3b2bfcf6fdf048916f2c0f7ae1ca1df7d70c59b3c2741`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 14.6 MB (14586410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb45ab9de2b51a3b30e5ce79b165b0ce68ef8949b3fb8747e0246e7f79aa44`  
		Last Modified: Wed, 13 May 2026 18:19:36 GMT  
		Size: 243.7 MB (243657701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5211313350d0e572d3e0e65222a070a4df6f33e34027e4a5b3ead5b3f127c5`  
		Last Modified: Wed, 13 May 2026 18:19:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5c394733d30386ce844be283abae53ff413c1ba31d59a88b68d52c56f7bc4881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13469d9da105c6b9de7b03110b854918d7fa9b8ef5bcdfcb6aca5afc6adfb93`

```dockerfile
```

-	Layers:
	-	`sha256:3f6eb045121c696ac20990b080b1c4beffd8134d73383c26f40d596d9dbd3cdb`  
		Last Modified: Wed, 13 May 2026 18:19:31 GMT  
		Size: 3.7 MB (3659871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04039a7799a89239c48a119c9f6c60a219c9cb8ae00532486897fa9bb5ab749c`  
		Last Modified: Wed, 13 May 2026 18:19:30 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0c7ee7de89f8d5b243583a28f142fd17034c113243b89e9bcf8c8dc4ebb4ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316071803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d7f750eb7cbc882e334b184174397bd69fc24fc5661a2184f12d68143217f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:17 GMT
ENV NODE_VERSION=22.22.2
# Wed, 15 Apr 2026 21:16:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:17 GMT
ENV YARN_VERSION=1.22.22
# Wed, 15 Apr 2026 21:16:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:16:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:16:21 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:46 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:49 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:49 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:01 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:01 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:43 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:43 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:43 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9bf56ef8e17f766ef1de2e4a09082317b49d5677cea5cc45b12665c6166b`  
		Last Modified: Wed, 15 Apr 2026 21:16:36 GMT  
		Size: 52.6 MB (52589162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153bc545a79f3ba26ea0150bb9bad2a7fd963de3c2ec2c543839c4142df1520`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52281c988abe43d0623753dd9e7fb5632481d23b16199148e12b237ba04da8`  
		Last Modified: Wed, 15 Apr 2026 21:16:35 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f1f8e5c163e88334b95732d2fbdaecf112a7b2fd09d9bba84d8481f3ca3a`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36277f504687f197adce49ac1646791597b88d8dda01c82afd413400e161cee0`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653949d9a736b846c26a75ea3b2fc3b89b9b4db6d7dc3f49643ce41fc1ae4b8`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 14.6 MB (14589078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bce99a94c661b02ebf66ae793284ead9ce5e584a772643978f4261d288a7a`  
		Last Modified: Wed, 13 May 2026 18:11:50 GMT  
		Size: 241.7 MB (241659148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7582f66fa5982c221a6ccfdf8ae5c0d2296d6aad82b7c9fc383a79c69eeb76`  
		Last Modified: Wed, 13 May 2026 18:11:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:db5aeb2b978df1e22e314dabda207eb92fce21035afc670a05f27f352f66773e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb9f8ac6baa138cfa692a7da41f77039b7c113201402d729a833c8687bd0d5`

```dockerfile
```

-	Layers:
	-	`sha256:0884c3fc6cd7f6835694270a0a3bdefc4df331a75afef5f1ca6b98a49447aeef`  
		Last Modified: Wed, 13 May 2026 18:11:44 GMT  
		Size: 3.7 MB (3659355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b107f5652fe0404bfe055c2e19fe7fb1fd905cd73a4f9677ec90ca86c2c3e2b0`  
		Last Modified: Wed, 13 May 2026 18:11:43 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:9e202d845c8ccd888d3a5df036945a754c00340399e77c2d18784142cf3926e3
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
$ docker pull ghost@sha256:7d6bdecb0217f9f2cad4c5f1af7a7ba43418d8d390e159c8255ba9570f5fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86398941a975f27fd8d1ffaf2ffb3fc3e5c36ecf9f5803b3adbf1b20ddaa276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:14 GMT
CMD ["node"]
# Wed, 13 May 2026 18:16:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:16:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:16:50 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:16:50 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:16:59 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:16:59 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:17:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:17:41 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:17:41 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:17:41 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:17:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a3aa5a9ad18507bf18000f0280556365b57788f03aca635c4792a79799082`  
		Last Modified: Fri, 08 May 2026 19:45:32 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c736fe2dee42f2274e133f0fd657bc3a2661f48b034a8adc2ba40bb6fa4b82`  
		Last Modified: Fri, 08 May 2026 19:46:30 GMT  
		Size: 49.8 MB (49837385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad35d9305371ac05c2bdf6de63217e78a5906a5f0335bd26432bbee187aea33`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e3008b73419a93cb985863971162eb59bcb78e57f6ef558fc198ad2848d89`  
		Last Modified: Fri, 08 May 2026 19:46:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf1ae69ce585605701a10b8da2932032512281981c3794c3731c69b6a78136`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 1.2 MB (1247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc189bdd63cdb11e9eece290d6d29c52bbbbfc93dba204b025cfd62b66e38c26`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 14.6 MB (14587402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d1a6d83207b7290bc66ba9f392b296edf0e51a03a82cf09e77eea5c3b0d9`  
		Last Modified: Wed, 13 May 2026 18:18:44 GMT  
		Size: 243.3 MB (243282009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb971e9e1687c78f68e3b1c9c6e447f5046a54aab5ea3e665943785230590778`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:b79125cae5cfec2a839ae8f2cdd14520a4e380ef2afe661886e047ad62c189bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e72ef291aafe6bf36baf614ec319f35fc08ec0d42e1e8c774e3962c7be3257`

```dockerfile
```

-	Layers:
	-	`sha256:682ee01ce95ce25a4751239551ee0dd3ee909641c2b4318a3c24553be760b29d`  
		Last Modified: Wed, 13 May 2026 18:18:39 GMT  
		Size: 5.9 MB (5871815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4c11b1e93d72c73a6ee5871d4971ad19b8f2b53c0b212ef978df24c3039ee3`  
		Last Modified: Wed, 13 May 2026 18:18:38 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:99fc74fe28e405f9ebb6d9871d5c774b35956a70b848c41e72bc679821ebcd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c357247b30577ae5f344e0d977ef5164346d86c9c705b4494351b22bac6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:46:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:22 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:46:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:46:35 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:37 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:37 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:50 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:50 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:13:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:13:09 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:13:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:13:09 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:13:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceab60b26d98607dbadb822874786541009e2c7508b79ba77ddba1369543c70`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08023a75f482d46de147f5741ec6f39bdc8b2bed59cbee01cc8021dad89349`  
		Last Modified: Fri, 08 May 2026 19:46:50 GMT  
		Size: 44.6 MB (44563952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff24056ee34abf0a8fb141f650e6f559a5fb011f8ba182ca048f430b62f59a`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 1.7 MB (1712840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a78c2ae5db1320d4577bdf21230559c2eb8c288cf910072bc423be5b1faecc`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d9c2f307dd7420a8063cb23ef06be1191264f343a7439b59069ec191a90b47`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 1.2 MB (1214394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b75230f318a7c1f7c8b68d60b1152ba43481a3efe66370d22a9ff728d175a`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 14.6 MB (14574185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf81cc6295e2b3dc87dfb2f8ad78216a07136090d3f5f44f4716a5c05cd83a4`  
		Last Modified: Wed, 13 May 2026 18:14:19 GMT  
		Size: 271.3 MB (271256754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c24fac299f05a76a9a878f9d4df54f8d8455e2456555d65b4f8930a11a14c`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:e26300dc5ed18f2a26c8b4bf00e8f018e09d81c630b2a521fdc437bc7eff40a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857159305f6e8151486e4e5f55d169c5c045bf8747e05806524a87152c2c0f62`

```dockerfile
```

-	Layers:
	-	`sha256:ff63b70e48598d55ed8e11fa80d56ec50308975fcf88ccd4984144925c6e6e4f`  
		Last Modified: Wed, 13 May 2026 18:14:13 GMT  
		Size: 5.9 MB (5877641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ebe3ab1184a8b3016ad8d7634d1f4784d0952699045ee666a8682d2e00d03a`  
		Last Modified: Wed, 13 May 2026 18:14:12 GMT  
		Size: 26.7 KB (26657 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e529a5df244060e05b266082f4a8645485a39aaddaa38eb195d2f6947e91813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337931039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d46226cc1f56a22fc23e554397000bed38141f59df1ee6df82b4c64daf8580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 19:47:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:39 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 19:47:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:51 GMT
CMD ["node"]
# Wed, 13 May 2026 18:09:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:09:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:09:53 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:09:53 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:05 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:05 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:10:50 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:10:50 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:10:50 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:10:50 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6b93c89baff7cfa8d6e7e163f9808d8483a292dcf5bedfebbeec6f03ed676`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2ac377c51591eb839dd9050d892160b182e934deae608e358a10234f2b5ed`  
		Last Modified: Fri, 08 May 2026 19:48:07 GMT  
		Size: 50.0 MB (49985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a880d93fcb99e440646721f6cc1fd56c579e28bc6c9bb6b79917aa64e23b8`  
		Last Modified: Fri, 08 May 2026 19:48:06 GMT  
		Size: 1.7 MB (1712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f8ff7ca0592a1bca5df81a5c864285584662deeaccc427ce3e87dbd2e630`  
		Last Modified: Fri, 08 May 2026 19:48:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edd4f8104fa5c7d2bc50bd440c6f1cf5332500f3ac22aff6e2a5e0134fd1d`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 1.2 MB (1201515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0de4f1abf0c4821e521d2860009e4d2606552e5078d9db516806e31fc57ef`  
		Last Modified: Wed, 13 May 2026 18:11:52 GMT  
		Size: 14.6 MB (14589917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033ec75d76040d1b4a148afae630b503689e9210abec0ee29a42df7f5f84e91`  
		Last Modified: Wed, 13 May 2026 18:11:59 GMT  
		Size: 242.3 MB (242320956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac58f5d1876bba422ac0def41b4e5e2c87249df1759c9c771f3c059402f9b7`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:a41ccaf6280e3bd797e256c4137c2d6d11fe3b7cce36a6b464b1f06a9fb83461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b94294d5d51a7d5bfecfbbc44a320d392526a14624b7b8077094546777a822`

```dockerfile
```

-	Layers:
	-	`sha256:44f1423513effe2d58a968816e05457bada96a5573313a850af88ba7b5048be5`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 5.9 MB (5872144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b589d40111b604647bb5130fe4c9cf7001c183eba3259edabd5a594e5cc1d8`  
		Last Modified: Wed, 13 May 2026 18:11:51 GMT  
		Size: 26.7 KB (26701 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:a0847fb57084bcd1bbc72974243b6639aa066b742a9e5ab2095a1384d35dd281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366025218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755dfff0921509171a415ffc9c2f44db62cf3e53ff5e43a0438bc919a127f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:59:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV NODE_VERSION=22.22.2
# Fri, 08 May 2026 21:02:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:44 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 May 2026 21:02:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 21:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 21:02:55 GMT
CMD ["node"]
# Wed, 13 May 2026 18:10:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:10:11 GMT
ENV NODE_ENV=production
# Wed, 13 May 2026 18:10:11 GMT
ENV GHOST_CLI_VERSION=1.29.2
# Wed, 13 May 2026 18:10:25 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 May 2026 18:10:25 GMT
ENV GHOST_VERSION=6.38.0
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Wed, 13 May 2026 18:12:35 GMT
WORKDIR /var/lib/ghost
# Wed, 13 May 2026 18:12:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 May 2026 18:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 May 2026 18:12:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c1a8b5ef0894cdc5aefe91ab600569cb955d2701ca45c6dff93c04eab2c05`  
		Last Modified: Fri, 08 May 2026 21:00:21 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6f742286b2b088f85df806d1cfda1c3a4cdff4dc2dd26018b948907abd0c1`  
		Last Modified: Fri, 08 May 2026 21:03:20 GMT  
		Size: 50.0 MB (50030802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dee5c88fea0d886c2692d09359177db5e6c64ca0436b571fbd9e772162210b`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a9b7b408f297ea04f188cfbaa029d85af72efcce2e78c4876ca345a68df6c`  
		Last Modified: Fri, 08 May 2026 21:03:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caed1cc86195a89a5f30e4df6f31807fdeef7466f2fce747278c6971d54ef10`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 1.2 MB (1221383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d6654b235f0c96c718df55fee6974c9cd96784e768c586d0d47b67de7dc5e`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 14.6 MB (14591987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40495036dd9c4c59b27600ba1dfb20fa51b3d8cb17d4de95e366b5d58d9d6663`  
		Last Modified: Wed, 13 May 2026 18:14:06 GMT  
		Size: 271.6 MB (271572448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31a1158ed4d3ad7c843d5a4b6573b65e912997804adba8a689cb4f6fc4751c`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:5f7ff3e49778e264499a5901bebe6c6d566f45ed1ae2e6991fd4a100a56e85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68be1c02a78599812c5570dfd7b144b097d527a51a0e51173d6b6a4c282b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fb6023e696db3be6e0076f8934617e76e4732cc87ff29646a386f8efcbd3f`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 5.9 MB (5868673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8950418f3ef18439f692a3025fb2881514d7725135e247635682c1bd0762e8b`  
		Last Modified: Wed, 13 May 2026 18:13:59 GMT  
		Size: 26.5 KB (26519 bytes)  
		MIME: application/vnd.in-toto+json

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5-alpine3.22`](#ghost5-alpine322)
-	[`ghost:5-bookworm`](#ghost5-bookworm)
-	[`ghost:5.130`](#ghost5130)
-	[`ghost:5.130-alpine`](#ghost5130-alpine)
-	[`ghost:5.130-alpine3.22`](#ghost5130-alpine322)
-	[`ghost:5.130-bookworm`](#ghost5130-bookworm)
-	[`ghost:5.130.5`](#ghost51305)
-	[`ghost:5.130.5-alpine`](#ghost51305-alpine)
-	[`ghost:5.130.5-alpine3.22`](#ghost51305-alpine322)
-	[`ghost:5.130.5-bookworm`](#ghost51305-bookworm)
-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.22`](#ghost6-alpine322)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.9`](#ghost69)
-	[`ghost:6.9-alpine`](#ghost69-alpine)
-	[`ghost:6.9-alpine3.22`](#ghost69-alpine322)
-	[`ghost:6.9-bookworm`](#ghost69-bookworm)
-	[`ghost:6.9.0`](#ghost690)
-	[`ghost:6.9.0-alpine`](#ghost690-alpine)
-	[`ghost:6.9.0-alpine3.22`](#ghost690-alpine322)
-	[`ghost:6.9.0-bookworm`](#ghost690-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.22`](#ghostalpine322)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:56f66947a25ae319380563bd762f1a68091444e4443c128016ec3e4afb018493
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

### `ghost:5` - linux; amd64

```console
$ docker pull ghost@sha256:16d75c50ccf97d39b2a0f6165d96f4bc1d0ca7e9618c679bf66de09693d4d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201286807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f1a5bb3d00c57a30546c5ac92310e230c6784fef54088ddfa65baf15244ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 05:31:20 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:31:31 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:31:31 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:33 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:10:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:10:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:10:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb6456a5555288c8c6e1aca9b3f6f1b7cf6b913009649e631c6d4134119561`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f691659c2173b66f66f5ecad6e0186f2638e15ecad4a73171e0f70838de5`  
		Last Modified: Tue, 18 Nov 2025 05:31:57 GMT  
		Size: 41.0 MB (40977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c3606ae6509cf726973a0d2f762b7f821b5426849318678222d85ab228f`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eecfc55be5f19d3b0967bb0ae0f53d17786b6a6ca7355d1ca3e9b97f77ca21`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36b986fb5eb5ed8f7fc039639341f395e63e47f0fbfde03007b249484144d0`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 1.2 MB (1247535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ed7f04cd1e7ac3499a45d0a483cfafa17867d4874f8c1f380161944938b2`  
		Last Modified: Tue, 18 Nov 2025 07:11:34 GMT  
		Size: 11.1 MB (11094625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0af66bf5ab650d8714ccdd11e6a2086d705c82edd02c242460ea8d2d426fac`  
		Last Modified: Tue, 18 Nov 2025 07:11:47 GMT  
		Size: 118.0 MB (118021441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea54a71b860144eea81cfd97d1135a14ca0bbb83dd582ae6557b6930b11dbf`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:138aea6a17b263cc6e6c03f54fe42013e7296baba8c0d09b6e6eab085c3cc568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9780c8cac6f79be6aa1a90b51b211a9bfb309b8db040fb7f97867f4acfdd`

```dockerfile
```

-	Layers:
	-	`sha256:dab95cf0370a2401c1e3aad57efaf0740129df26a05de57c000e4848747922e2`  
		Last Modified: Tue, 18 Nov 2025 10:45:58 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180199b9d7d9a2c97d4765664c63152bbc8c83bbefbda4ae8f05dc361ede9ad7`  
		Last Modified: Tue, 18 Nov 2025 10:45:59 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1b4b775e74d10caf91f1bf765826141ae222217a7120f958be4889db0624a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0af20fe06eb7b266bdbdb97e8774edeba1fc0732afc52be23e7c47fcb5331c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:23:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:59 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:41 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:29:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527544c5654513868ce4d87aa5d977a07b324ed7c909b8b723f87bb633ed7c6d`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bc82fd181b9997e60069bdef220be82aaf6f3f2b2085d94a3f9dec8b0a013`  
		Last Modified: Tue, 18 Nov 2025 04:24:18 GMT  
		Size: 37.1 MB (37064246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185456839ac256b05beb1e5b4e9a21be6c7f93534d8b9293a2c7759a4e520fc`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de307c97b77fdeaae17f0a556c74372c6872926ec6f33d52b8e7e7642142e7a`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3df8febaf6b4464745efcc043c420cbb59e26e46dfd5d92b47678316dc5bb9`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c22ea2410de9defd76065b35423ca9f81e0a93d0e15e43f57cf102820f958`  
		Last Modified: Tue, 18 Nov 2025 07:30:30 GMT  
		Size: 11.1 MB (11095341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94606ad0102f1fa85b85732ce6811fb461085d590769d0105bde4388cbda7600`  
		Last Modified: Tue, 18 Nov 2025 07:30:45 GMT  
		Size: 120.6 MB (120587361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cdc0ff3787f0b0d0e2784efd40bbbbb74d8301bf9a139c673dee991c2ec5ea`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:18e60ff0419a941f8422caf3fb52687bf2a32462d300662da85a31a510b47da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52791ac377ea7bf1aeb7d7e92be934f93d567079e43f324e58fedc4db47d50`

```dockerfile
```

-	Layers:
	-	`sha256:0adde6bfd8460b8e525d122595aedad639d4882fc6723e3dfb86ee09d72024e8`  
		Last Modified: Tue, 18 Nov 2025 10:46:04 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb59777b002fbb9144a4df92f1878f7952c03a391fc95c41a000f07367e6449`  
		Last Modified: Tue, 18 Nov 2025 10:46:05 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cbae22d4c2275e7096343d19b07327bad9a1f2058b7b3233ba160d37c0791be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8c41799de687d9a67018cac858432aa0fef8f73342dd28e1ba390976e351d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:00:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:05:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:05:49 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:49 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 06:17:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:17:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:37 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:17:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151457d95a5866436937e5d27d506481b8563d00b639fb2b4a8c40a19071660b`  
		Last Modified: Tue, 18 Nov 2025 04:01:26 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658d3794cdbd4098e62f50f063ad1c77daee5aa96e3ae3c0720ec13f6f79481`  
		Last Modified: Tue, 18 Nov 2025 04:06:13 GMT  
		Size: 40.9 MB (40939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa13d1b8fcd7d01146fd5b5064fca5a15d13ebfaa4ed43bbb17ad41c9acf21`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56134264619c5f9d99719f23af9471427ea7291468c759595f5c1f1757e7af`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4caacac319447ed5cef1dacae670a1810faa81f77daee3fa4d8849d87316b`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 1.2 MB (1201442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9667cd483d44b60c37d87171e051c983d6916306152a0f527911d7b84a846`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 11.1 MB (11094321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a711a2c6e373b6f1353f031f12e5d703d7703db7940b20eaacfb3097bfbc9c0`  
		Last Modified: Tue, 18 Nov 2025 06:18:35 GMT  
		Size: 118.1 MB (118116320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e854d6b9608165241a45ac9cccd1dbfa3db3bb8173f7ff572ce7f636285f2`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:c39838fb1a8fabc3864e085dc68277ca83d0d360e4528e4dc0d0dfc4d71219ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365c43e8ea0119666083fe9f9d70ce72742706ee55bfbe12d547884e8478d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0f386aace00ef7209fc42e8be14e478d1ae07bfce1215281240047c56d66e6d`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257dba59896dc8affe970c1b9a7a7488b39599bcadcdf8776dbb084ad18d633`  
		Last Modified: Tue, 18 Nov 2025 07:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:f5dc675ba48f5dd47f1746a39a49de73f28a6d8dc0a303cb95017be34b39f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204796779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68050bc4785676a3d0d88a86f7e734771f1c89f72c8853639756a5834f29c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:09:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:13:05 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:13:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:13:14 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:06 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:03:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:35 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d683f4d5080591112b5d19b1b5db2cb7a3d8c47400239407275302d454723f`  
		Last Modified: Tue, 18 Nov 2025 04:10:16 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a3cb3febab65c9bfc8547f93ad9971b384a53c66394ff3a9365a94c74bf19f`  
		Last Modified: Tue, 18 Nov 2025 04:13:43 GMT  
		Size: 41.2 MB (41222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7e39c24509f77776773739aa5bbe814d3e2de93b548ef745ce4bfa44141e9`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 1.7 MB (1712597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2351955604b7ebd37554987c778e617da52b3e8292c6497b1a45243accb6979`  
		Last Modified: Tue, 18 Nov 2025 04:13:39 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee6f822e10fe4fd83989957020a3eca9e0e3ebb7b2e5ad31a9904ec6648714`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 1.2 MB (1221459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fc65be1b596b43240d8b3b08b53fc04f1790dfb7edeaa79b4979e20bae582`  
		Last Modified: Tue, 18 Nov 2025 07:05:24 GMT  
		Size: 11.1 MB (11100261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80eb9144360a07a0c2d8ee8d2780d6f6515f75448e3aab15274b399c213d9`  
		Last Modified: Tue, 18 Nov 2025 07:05:32 GMT  
		Size: 122.7 MB (122651217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226fc85fb3e82ee136221e21f0dfa416f0586db51f30fe20d9915472868dba1`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:36db1953f673e6a4ef29bd80ca3aaefc59f938f541ba4eb3d1a762fa295af3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a7ba99a444e4af864970bfb957e659c7fd89ad91d19c0c124f073dec925d7`

```dockerfile
```

-	Layers:
	-	`sha256:25c88537d8040044f3c95cd023525fcef6b96a5803bbda714520587a236302ec`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702cbca7c5996b9b78c1962b0a85f89383bd30cc0bca27e602c8e2d56c3872a`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine3.22`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-bookworm`

```console
$ docker pull ghost@sha256:56f66947a25ae319380563bd762f1a68091444e4443c128016ec3e4afb018493
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

### `ghost:5-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:16d75c50ccf97d39b2a0f6165d96f4bc1d0ca7e9618c679bf66de09693d4d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201286807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f1a5bb3d00c57a30546c5ac92310e230c6784fef54088ddfa65baf15244ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 05:31:20 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:31:31 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:31:31 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:33 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:10:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:10:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:10:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb6456a5555288c8c6e1aca9b3f6f1b7cf6b913009649e631c6d4134119561`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f691659c2173b66f66f5ecad6e0186f2638e15ecad4a73171e0f70838de5`  
		Last Modified: Tue, 18 Nov 2025 05:31:57 GMT  
		Size: 41.0 MB (40977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c3606ae6509cf726973a0d2f762b7f821b5426849318678222d85ab228f`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eecfc55be5f19d3b0967bb0ae0f53d17786b6a6ca7355d1ca3e9b97f77ca21`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36b986fb5eb5ed8f7fc039639341f395e63e47f0fbfde03007b249484144d0`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 1.2 MB (1247535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ed7f04cd1e7ac3499a45d0a483cfafa17867d4874f8c1f380161944938b2`  
		Last Modified: Tue, 18 Nov 2025 07:11:34 GMT  
		Size: 11.1 MB (11094625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0af66bf5ab650d8714ccdd11e6a2086d705c82edd02c242460ea8d2d426fac`  
		Last Modified: Tue, 18 Nov 2025 07:11:47 GMT  
		Size: 118.0 MB (118021441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea54a71b860144eea81cfd97d1135a14ca0bbb83dd582ae6557b6930b11dbf`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:138aea6a17b263cc6e6c03f54fe42013e7296baba8c0d09b6e6eab085c3cc568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9780c8cac6f79be6aa1a90b51b211a9bfb309b8db040fb7f97867f4acfdd`

```dockerfile
```

-	Layers:
	-	`sha256:dab95cf0370a2401c1e3aad57efaf0740129df26a05de57c000e4848747922e2`  
		Last Modified: Tue, 18 Nov 2025 10:45:58 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180199b9d7d9a2c97d4765664c63152bbc8c83bbefbda4ae8f05dc361ede9ad7`  
		Last Modified: Tue, 18 Nov 2025 10:45:59 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1b4b775e74d10caf91f1bf765826141ae222217a7120f958be4889db0624a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0af20fe06eb7b266bdbdb97e8774edeba1fc0732afc52be23e7c47fcb5331c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:23:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:59 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:41 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:29:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527544c5654513868ce4d87aa5d977a07b324ed7c909b8b723f87bb633ed7c6d`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bc82fd181b9997e60069bdef220be82aaf6f3f2b2085d94a3f9dec8b0a013`  
		Last Modified: Tue, 18 Nov 2025 04:24:18 GMT  
		Size: 37.1 MB (37064246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185456839ac256b05beb1e5b4e9a21be6c7f93534d8b9293a2c7759a4e520fc`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de307c97b77fdeaae17f0a556c74372c6872926ec6f33d52b8e7e7642142e7a`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3df8febaf6b4464745efcc043c420cbb59e26e46dfd5d92b47678316dc5bb9`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c22ea2410de9defd76065b35423ca9f81e0a93d0e15e43f57cf102820f958`  
		Last Modified: Tue, 18 Nov 2025 07:30:30 GMT  
		Size: 11.1 MB (11095341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94606ad0102f1fa85b85732ce6811fb461085d590769d0105bde4388cbda7600`  
		Last Modified: Tue, 18 Nov 2025 07:30:45 GMT  
		Size: 120.6 MB (120587361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cdc0ff3787f0b0d0e2784efd40bbbbb74d8301bf9a139c673dee991c2ec5ea`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:18e60ff0419a941f8422caf3fb52687bf2a32462d300662da85a31a510b47da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52791ac377ea7bf1aeb7d7e92be934f93d567079e43f324e58fedc4db47d50`

```dockerfile
```

-	Layers:
	-	`sha256:0adde6bfd8460b8e525d122595aedad639d4882fc6723e3dfb86ee09d72024e8`  
		Last Modified: Tue, 18 Nov 2025 10:46:04 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb59777b002fbb9144a4df92f1878f7952c03a391fc95c41a000f07367e6449`  
		Last Modified: Tue, 18 Nov 2025 10:46:05 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cbae22d4c2275e7096343d19b07327bad9a1f2058b7b3233ba160d37c0791be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8c41799de687d9a67018cac858432aa0fef8f73342dd28e1ba390976e351d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:00:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:05:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:05:49 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:49 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 06:17:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:17:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:37 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:17:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151457d95a5866436937e5d27d506481b8563d00b639fb2b4a8c40a19071660b`  
		Last Modified: Tue, 18 Nov 2025 04:01:26 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658d3794cdbd4098e62f50f063ad1c77daee5aa96e3ae3c0720ec13f6f79481`  
		Last Modified: Tue, 18 Nov 2025 04:06:13 GMT  
		Size: 40.9 MB (40939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa13d1b8fcd7d01146fd5b5064fca5a15d13ebfaa4ed43bbb17ad41c9acf21`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56134264619c5f9d99719f23af9471427ea7291468c759595f5c1f1757e7af`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4caacac319447ed5cef1dacae670a1810faa81f77daee3fa4d8849d87316b`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 1.2 MB (1201442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9667cd483d44b60c37d87171e051c983d6916306152a0f527911d7b84a846`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 11.1 MB (11094321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a711a2c6e373b6f1353f031f12e5d703d7703db7940b20eaacfb3097bfbc9c0`  
		Last Modified: Tue, 18 Nov 2025 06:18:35 GMT  
		Size: 118.1 MB (118116320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e854d6b9608165241a45ac9cccd1dbfa3db3bb8173f7ff572ce7f636285f2`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c39838fb1a8fabc3864e085dc68277ca83d0d360e4528e4dc0d0dfc4d71219ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365c43e8ea0119666083fe9f9d70ce72742706ee55bfbe12d547884e8478d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0f386aace00ef7209fc42e8be14e478d1ae07bfce1215281240047c56d66e6d`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257dba59896dc8affe970c1b9a7a7488b39599bcadcdf8776dbb084ad18d633`  
		Last Modified: Tue, 18 Nov 2025 07:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:f5dc675ba48f5dd47f1746a39a49de73f28a6d8dc0a303cb95017be34b39f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204796779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68050bc4785676a3d0d88a86f7e734771f1c89f72c8853639756a5834f29c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:09:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:13:05 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:13:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:13:14 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:06 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:03:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:35 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d683f4d5080591112b5d19b1b5db2cb7a3d8c47400239407275302d454723f`  
		Last Modified: Tue, 18 Nov 2025 04:10:16 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a3cb3febab65c9bfc8547f93ad9971b384a53c66394ff3a9365a94c74bf19f`  
		Last Modified: Tue, 18 Nov 2025 04:13:43 GMT  
		Size: 41.2 MB (41222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7e39c24509f77776773739aa5bbe814d3e2de93b548ef745ce4bfa44141e9`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 1.7 MB (1712597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2351955604b7ebd37554987c778e617da52b3e8292c6497b1a45243accb6979`  
		Last Modified: Tue, 18 Nov 2025 04:13:39 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee6f822e10fe4fd83989957020a3eca9e0e3ebb7b2e5ad31a9904ec6648714`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 1.2 MB (1221459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fc65be1b596b43240d8b3b08b53fc04f1790dfb7edeaa79b4979e20bae582`  
		Last Modified: Tue, 18 Nov 2025 07:05:24 GMT  
		Size: 11.1 MB (11100261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80eb9144360a07a0c2d8ee8d2780d6f6515f75448e3aab15274b399c213d9`  
		Last Modified: Tue, 18 Nov 2025 07:05:32 GMT  
		Size: 122.7 MB (122651217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226fc85fb3e82ee136221e21f0dfa416f0586db51f30fe20d9915472868dba1`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:36db1953f673e6a4ef29bd80ca3aaefc59f938f541ba4eb3d1a762fa295af3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a7ba99a444e4af864970bfb957e659c7fd89ad91d19c0c124f073dec925d7`

```dockerfile
```

-	Layers:
	-	`sha256:25c88537d8040044f3c95cd023525fcef6b96a5803bbda714520587a236302ec`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702cbca7c5996b9b78c1962b0a85f89383bd30cc0bca27e602c8e2d56c3872a`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130`

```console
$ docker pull ghost@sha256:56f66947a25ae319380563bd762f1a68091444e4443c128016ec3e4afb018493
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

### `ghost:5.130` - linux; amd64

```console
$ docker pull ghost@sha256:16d75c50ccf97d39b2a0f6165d96f4bc1d0ca7e9618c679bf66de09693d4d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201286807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f1a5bb3d00c57a30546c5ac92310e230c6784fef54088ddfa65baf15244ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 05:31:20 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:31:31 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:31:31 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:33 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:10:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:10:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:10:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb6456a5555288c8c6e1aca9b3f6f1b7cf6b913009649e631c6d4134119561`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f691659c2173b66f66f5ecad6e0186f2638e15ecad4a73171e0f70838de5`  
		Last Modified: Tue, 18 Nov 2025 05:31:57 GMT  
		Size: 41.0 MB (40977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c3606ae6509cf726973a0d2f762b7f821b5426849318678222d85ab228f`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eecfc55be5f19d3b0967bb0ae0f53d17786b6a6ca7355d1ca3e9b97f77ca21`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36b986fb5eb5ed8f7fc039639341f395e63e47f0fbfde03007b249484144d0`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 1.2 MB (1247535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ed7f04cd1e7ac3499a45d0a483cfafa17867d4874f8c1f380161944938b2`  
		Last Modified: Tue, 18 Nov 2025 07:11:34 GMT  
		Size: 11.1 MB (11094625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0af66bf5ab650d8714ccdd11e6a2086d705c82edd02c242460ea8d2d426fac`  
		Last Modified: Tue, 18 Nov 2025 07:11:47 GMT  
		Size: 118.0 MB (118021441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea54a71b860144eea81cfd97d1135a14ca0bbb83dd582ae6557b6930b11dbf`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:138aea6a17b263cc6e6c03f54fe42013e7296baba8c0d09b6e6eab085c3cc568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9780c8cac6f79be6aa1a90b51b211a9bfb309b8db040fb7f97867f4acfdd`

```dockerfile
```

-	Layers:
	-	`sha256:dab95cf0370a2401c1e3aad57efaf0740129df26a05de57c000e4848747922e2`  
		Last Modified: Tue, 18 Nov 2025 10:45:58 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180199b9d7d9a2c97d4765664c63152bbc8c83bbefbda4ae8f05dc361ede9ad7`  
		Last Modified: Tue, 18 Nov 2025 10:45:59 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1b4b775e74d10caf91f1bf765826141ae222217a7120f958be4889db0624a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0af20fe06eb7b266bdbdb97e8774edeba1fc0732afc52be23e7c47fcb5331c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:23:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:59 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:41 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:29:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527544c5654513868ce4d87aa5d977a07b324ed7c909b8b723f87bb633ed7c6d`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bc82fd181b9997e60069bdef220be82aaf6f3f2b2085d94a3f9dec8b0a013`  
		Last Modified: Tue, 18 Nov 2025 04:24:18 GMT  
		Size: 37.1 MB (37064246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185456839ac256b05beb1e5b4e9a21be6c7f93534d8b9293a2c7759a4e520fc`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de307c97b77fdeaae17f0a556c74372c6872926ec6f33d52b8e7e7642142e7a`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3df8febaf6b4464745efcc043c420cbb59e26e46dfd5d92b47678316dc5bb9`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c22ea2410de9defd76065b35423ca9f81e0a93d0e15e43f57cf102820f958`  
		Last Modified: Tue, 18 Nov 2025 07:30:30 GMT  
		Size: 11.1 MB (11095341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94606ad0102f1fa85b85732ce6811fb461085d590769d0105bde4388cbda7600`  
		Last Modified: Tue, 18 Nov 2025 07:30:45 GMT  
		Size: 120.6 MB (120587361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cdc0ff3787f0b0d0e2784efd40bbbbb74d8301bf9a139c673dee991c2ec5ea`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:18e60ff0419a941f8422caf3fb52687bf2a32462d300662da85a31a510b47da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52791ac377ea7bf1aeb7d7e92be934f93d567079e43f324e58fedc4db47d50`

```dockerfile
```

-	Layers:
	-	`sha256:0adde6bfd8460b8e525d122595aedad639d4882fc6723e3dfb86ee09d72024e8`  
		Last Modified: Tue, 18 Nov 2025 10:46:04 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb59777b002fbb9144a4df92f1878f7952c03a391fc95c41a000f07367e6449`  
		Last Modified: Tue, 18 Nov 2025 10:46:05 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cbae22d4c2275e7096343d19b07327bad9a1f2058b7b3233ba160d37c0791be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8c41799de687d9a67018cac858432aa0fef8f73342dd28e1ba390976e351d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:00:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:05:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:05:49 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:49 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 06:17:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:17:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:37 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:17:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151457d95a5866436937e5d27d506481b8563d00b639fb2b4a8c40a19071660b`  
		Last Modified: Tue, 18 Nov 2025 04:01:26 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658d3794cdbd4098e62f50f063ad1c77daee5aa96e3ae3c0720ec13f6f79481`  
		Last Modified: Tue, 18 Nov 2025 04:06:13 GMT  
		Size: 40.9 MB (40939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa13d1b8fcd7d01146fd5b5064fca5a15d13ebfaa4ed43bbb17ad41c9acf21`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56134264619c5f9d99719f23af9471427ea7291468c759595f5c1f1757e7af`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4caacac319447ed5cef1dacae670a1810faa81f77daee3fa4d8849d87316b`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 1.2 MB (1201442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9667cd483d44b60c37d87171e051c983d6916306152a0f527911d7b84a846`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 11.1 MB (11094321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a711a2c6e373b6f1353f031f12e5d703d7703db7940b20eaacfb3097bfbc9c0`  
		Last Modified: Tue, 18 Nov 2025 06:18:35 GMT  
		Size: 118.1 MB (118116320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e854d6b9608165241a45ac9cccd1dbfa3db3bb8173f7ff572ce7f636285f2`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:c39838fb1a8fabc3864e085dc68277ca83d0d360e4528e4dc0d0dfc4d71219ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365c43e8ea0119666083fe9f9d70ce72742706ee55bfbe12d547884e8478d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0f386aace00ef7209fc42e8be14e478d1ae07bfce1215281240047c56d66e6d`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257dba59896dc8affe970c1b9a7a7488b39599bcadcdf8776dbb084ad18d633`  
		Last Modified: Tue, 18 Nov 2025 07:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; s390x

```console
$ docker pull ghost@sha256:f5dc675ba48f5dd47f1746a39a49de73f28a6d8dc0a303cb95017be34b39f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204796779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68050bc4785676a3d0d88a86f7e734771f1c89f72c8853639756a5834f29c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:09:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:13:05 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:13:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:13:14 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:06 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:03:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:35 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d683f4d5080591112b5d19b1b5db2cb7a3d8c47400239407275302d454723f`  
		Last Modified: Tue, 18 Nov 2025 04:10:16 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a3cb3febab65c9bfc8547f93ad9971b384a53c66394ff3a9365a94c74bf19f`  
		Last Modified: Tue, 18 Nov 2025 04:13:43 GMT  
		Size: 41.2 MB (41222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7e39c24509f77776773739aa5bbe814d3e2de93b548ef745ce4bfa44141e9`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 1.7 MB (1712597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2351955604b7ebd37554987c778e617da52b3e8292c6497b1a45243accb6979`  
		Last Modified: Tue, 18 Nov 2025 04:13:39 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee6f822e10fe4fd83989957020a3eca9e0e3ebb7b2e5ad31a9904ec6648714`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 1.2 MB (1221459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fc65be1b596b43240d8b3b08b53fc04f1790dfb7edeaa79b4979e20bae582`  
		Last Modified: Tue, 18 Nov 2025 07:05:24 GMT  
		Size: 11.1 MB (11100261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80eb9144360a07a0c2d8ee8d2780d6f6515f75448e3aab15274b399c213d9`  
		Last Modified: Tue, 18 Nov 2025 07:05:32 GMT  
		Size: 122.7 MB (122651217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226fc85fb3e82ee136221e21f0dfa416f0586db51f30fe20d9915472868dba1`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:36db1953f673e6a4ef29bd80ca3aaefc59f938f541ba4eb3d1a762fa295af3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a7ba99a444e4af864970bfb957e659c7fd89ad91d19c0c124f073dec925d7`

```dockerfile
```

-	Layers:
	-	`sha256:25c88537d8040044f3c95cd023525fcef6b96a5803bbda714520587a236302ec`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702cbca7c5996b9b78c1962b0a85f89383bd30cc0bca27e602c8e2d56c3872a`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine3.22`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-bookworm`

```console
$ docker pull ghost@sha256:56f66947a25ae319380563bd762f1a68091444e4443c128016ec3e4afb018493
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

### `ghost:5.130-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:16d75c50ccf97d39b2a0f6165d96f4bc1d0ca7e9618c679bf66de09693d4d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201286807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f1a5bb3d00c57a30546c5ac92310e230c6784fef54088ddfa65baf15244ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 05:31:20 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:31:31 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:31:31 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:33 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:10:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:10:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:10:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb6456a5555288c8c6e1aca9b3f6f1b7cf6b913009649e631c6d4134119561`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f691659c2173b66f66f5ecad6e0186f2638e15ecad4a73171e0f70838de5`  
		Last Modified: Tue, 18 Nov 2025 05:31:57 GMT  
		Size: 41.0 MB (40977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c3606ae6509cf726973a0d2f762b7f821b5426849318678222d85ab228f`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eecfc55be5f19d3b0967bb0ae0f53d17786b6a6ca7355d1ca3e9b97f77ca21`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36b986fb5eb5ed8f7fc039639341f395e63e47f0fbfde03007b249484144d0`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 1.2 MB (1247535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ed7f04cd1e7ac3499a45d0a483cfafa17867d4874f8c1f380161944938b2`  
		Last Modified: Tue, 18 Nov 2025 07:11:34 GMT  
		Size: 11.1 MB (11094625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0af66bf5ab650d8714ccdd11e6a2086d705c82edd02c242460ea8d2d426fac`  
		Last Modified: Tue, 18 Nov 2025 07:11:47 GMT  
		Size: 118.0 MB (118021441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea54a71b860144eea81cfd97d1135a14ca0bbb83dd582ae6557b6930b11dbf`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:138aea6a17b263cc6e6c03f54fe42013e7296baba8c0d09b6e6eab085c3cc568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9780c8cac6f79be6aa1a90b51b211a9bfb309b8db040fb7f97867f4acfdd`

```dockerfile
```

-	Layers:
	-	`sha256:dab95cf0370a2401c1e3aad57efaf0740129df26a05de57c000e4848747922e2`  
		Last Modified: Tue, 18 Nov 2025 10:45:58 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180199b9d7d9a2c97d4765664c63152bbc8c83bbefbda4ae8f05dc361ede9ad7`  
		Last Modified: Tue, 18 Nov 2025 10:45:59 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1b4b775e74d10caf91f1bf765826141ae222217a7120f958be4889db0624a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0af20fe06eb7b266bdbdb97e8774edeba1fc0732afc52be23e7c47fcb5331c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:23:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:59 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:41 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:29:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527544c5654513868ce4d87aa5d977a07b324ed7c909b8b723f87bb633ed7c6d`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bc82fd181b9997e60069bdef220be82aaf6f3f2b2085d94a3f9dec8b0a013`  
		Last Modified: Tue, 18 Nov 2025 04:24:18 GMT  
		Size: 37.1 MB (37064246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185456839ac256b05beb1e5b4e9a21be6c7f93534d8b9293a2c7759a4e520fc`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de307c97b77fdeaae17f0a556c74372c6872926ec6f33d52b8e7e7642142e7a`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3df8febaf6b4464745efcc043c420cbb59e26e46dfd5d92b47678316dc5bb9`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c22ea2410de9defd76065b35423ca9f81e0a93d0e15e43f57cf102820f958`  
		Last Modified: Tue, 18 Nov 2025 07:30:30 GMT  
		Size: 11.1 MB (11095341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94606ad0102f1fa85b85732ce6811fb461085d590769d0105bde4388cbda7600`  
		Last Modified: Tue, 18 Nov 2025 07:30:45 GMT  
		Size: 120.6 MB (120587361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cdc0ff3787f0b0d0e2784efd40bbbbb74d8301bf9a139c673dee991c2ec5ea`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:18e60ff0419a941f8422caf3fb52687bf2a32462d300662da85a31a510b47da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52791ac377ea7bf1aeb7d7e92be934f93d567079e43f324e58fedc4db47d50`

```dockerfile
```

-	Layers:
	-	`sha256:0adde6bfd8460b8e525d122595aedad639d4882fc6723e3dfb86ee09d72024e8`  
		Last Modified: Tue, 18 Nov 2025 10:46:04 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb59777b002fbb9144a4df92f1878f7952c03a391fc95c41a000f07367e6449`  
		Last Modified: Tue, 18 Nov 2025 10:46:05 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cbae22d4c2275e7096343d19b07327bad9a1f2058b7b3233ba160d37c0791be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8c41799de687d9a67018cac858432aa0fef8f73342dd28e1ba390976e351d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:00:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:05:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:05:49 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:49 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 06:17:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:17:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:37 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:17:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151457d95a5866436937e5d27d506481b8563d00b639fb2b4a8c40a19071660b`  
		Last Modified: Tue, 18 Nov 2025 04:01:26 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658d3794cdbd4098e62f50f063ad1c77daee5aa96e3ae3c0720ec13f6f79481`  
		Last Modified: Tue, 18 Nov 2025 04:06:13 GMT  
		Size: 40.9 MB (40939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa13d1b8fcd7d01146fd5b5064fca5a15d13ebfaa4ed43bbb17ad41c9acf21`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56134264619c5f9d99719f23af9471427ea7291468c759595f5c1f1757e7af`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4caacac319447ed5cef1dacae670a1810faa81f77daee3fa4d8849d87316b`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 1.2 MB (1201442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9667cd483d44b60c37d87171e051c983d6916306152a0f527911d7b84a846`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 11.1 MB (11094321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a711a2c6e373b6f1353f031f12e5d703d7703db7940b20eaacfb3097bfbc9c0`  
		Last Modified: Tue, 18 Nov 2025 06:18:35 GMT  
		Size: 118.1 MB (118116320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e854d6b9608165241a45ac9cccd1dbfa3db3bb8173f7ff572ce7f636285f2`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c39838fb1a8fabc3864e085dc68277ca83d0d360e4528e4dc0d0dfc4d71219ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365c43e8ea0119666083fe9f9d70ce72742706ee55bfbe12d547884e8478d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0f386aace00ef7209fc42e8be14e478d1ae07bfce1215281240047c56d66e6d`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257dba59896dc8affe970c1b9a7a7488b39599bcadcdf8776dbb084ad18d633`  
		Last Modified: Tue, 18 Nov 2025 07:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:f5dc675ba48f5dd47f1746a39a49de73f28a6d8dc0a303cb95017be34b39f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204796779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68050bc4785676a3d0d88a86f7e734771f1c89f72c8853639756a5834f29c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:09:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:13:05 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:13:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:13:14 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:06 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:03:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:35 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d683f4d5080591112b5d19b1b5db2cb7a3d8c47400239407275302d454723f`  
		Last Modified: Tue, 18 Nov 2025 04:10:16 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a3cb3febab65c9bfc8547f93ad9971b384a53c66394ff3a9365a94c74bf19f`  
		Last Modified: Tue, 18 Nov 2025 04:13:43 GMT  
		Size: 41.2 MB (41222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7e39c24509f77776773739aa5bbe814d3e2de93b548ef745ce4bfa44141e9`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 1.7 MB (1712597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2351955604b7ebd37554987c778e617da52b3e8292c6497b1a45243accb6979`  
		Last Modified: Tue, 18 Nov 2025 04:13:39 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee6f822e10fe4fd83989957020a3eca9e0e3ebb7b2e5ad31a9904ec6648714`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 1.2 MB (1221459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fc65be1b596b43240d8b3b08b53fc04f1790dfb7edeaa79b4979e20bae582`  
		Last Modified: Tue, 18 Nov 2025 07:05:24 GMT  
		Size: 11.1 MB (11100261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80eb9144360a07a0c2d8ee8d2780d6f6515f75448e3aab15274b399c213d9`  
		Last Modified: Tue, 18 Nov 2025 07:05:32 GMT  
		Size: 122.7 MB (122651217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226fc85fb3e82ee136221e21f0dfa416f0586db51f30fe20d9915472868dba1`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:36db1953f673e6a4ef29bd80ca3aaefc59f938f541ba4eb3d1a762fa295af3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a7ba99a444e4af864970bfb957e659c7fd89ad91d19c0c124f073dec925d7`

```dockerfile
```

-	Layers:
	-	`sha256:25c88537d8040044f3c95cd023525fcef6b96a5803bbda714520587a236302ec`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702cbca7c5996b9b78c1962b0a85f89383bd30cc0bca27e602c8e2d56c3872a`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5`

```console
$ docker pull ghost@sha256:56f66947a25ae319380563bd762f1a68091444e4443c128016ec3e4afb018493
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

### `ghost:5.130.5` - linux; amd64

```console
$ docker pull ghost@sha256:16d75c50ccf97d39b2a0f6165d96f4bc1d0ca7e9618c679bf66de09693d4d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201286807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f1a5bb3d00c57a30546c5ac92310e230c6784fef54088ddfa65baf15244ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 05:31:20 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:31:31 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:31:31 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:33 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:10:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:10:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:10:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb6456a5555288c8c6e1aca9b3f6f1b7cf6b913009649e631c6d4134119561`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f691659c2173b66f66f5ecad6e0186f2638e15ecad4a73171e0f70838de5`  
		Last Modified: Tue, 18 Nov 2025 05:31:57 GMT  
		Size: 41.0 MB (40977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c3606ae6509cf726973a0d2f762b7f821b5426849318678222d85ab228f`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eecfc55be5f19d3b0967bb0ae0f53d17786b6a6ca7355d1ca3e9b97f77ca21`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36b986fb5eb5ed8f7fc039639341f395e63e47f0fbfde03007b249484144d0`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 1.2 MB (1247535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ed7f04cd1e7ac3499a45d0a483cfafa17867d4874f8c1f380161944938b2`  
		Last Modified: Tue, 18 Nov 2025 07:11:34 GMT  
		Size: 11.1 MB (11094625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0af66bf5ab650d8714ccdd11e6a2086d705c82edd02c242460ea8d2d426fac`  
		Last Modified: Tue, 18 Nov 2025 07:11:47 GMT  
		Size: 118.0 MB (118021441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea54a71b860144eea81cfd97d1135a14ca0bbb83dd582ae6557b6930b11dbf`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:138aea6a17b263cc6e6c03f54fe42013e7296baba8c0d09b6e6eab085c3cc568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9780c8cac6f79be6aa1a90b51b211a9bfb309b8db040fb7f97867f4acfdd`

```dockerfile
```

-	Layers:
	-	`sha256:dab95cf0370a2401c1e3aad57efaf0740129df26a05de57c000e4848747922e2`  
		Last Modified: Tue, 18 Nov 2025 10:45:58 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180199b9d7d9a2c97d4765664c63152bbc8c83bbefbda4ae8f05dc361ede9ad7`  
		Last Modified: Tue, 18 Nov 2025 10:45:59 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1b4b775e74d10caf91f1bf765826141ae222217a7120f958be4889db0624a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0af20fe06eb7b266bdbdb97e8774edeba1fc0732afc52be23e7c47fcb5331c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:23:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:59 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:41 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:29:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527544c5654513868ce4d87aa5d977a07b324ed7c909b8b723f87bb633ed7c6d`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bc82fd181b9997e60069bdef220be82aaf6f3f2b2085d94a3f9dec8b0a013`  
		Last Modified: Tue, 18 Nov 2025 04:24:18 GMT  
		Size: 37.1 MB (37064246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185456839ac256b05beb1e5b4e9a21be6c7f93534d8b9293a2c7759a4e520fc`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de307c97b77fdeaae17f0a556c74372c6872926ec6f33d52b8e7e7642142e7a`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3df8febaf6b4464745efcc043c420cbb59e26e46dfd5d92b47678316dc5bb9`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c22ea2410de9defd76065b35423ca9f81e0a93d0e15e43f57cf102820f958`  
		Last Modified: Tue, 18 Nov 2025 07:30:30 GMT  
		Size: 11.1 MB (11095341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94606ad0102f1fa85b85732ce6811fb461085d590769d0105bde4388cbda7600`  
		Last Modified: Tue, 18 Nov 2025 07:30:45 GMT  
		Size: 120.6 MB (120587361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cdc0ff3787f0b0d0e2784efd40bbbbb74d8301bf9a139c673dee991c2ec5ea`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:18e60ff0419a941f8422caf3fb52687bf2a32462d300662da85a31a510b47da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52791ac377ea7bf1aeb7d7e92be934f93d567079e43f324e58fedc4db47d50`

```dockerfile
```

-	Layers:
	-	`sha256:0adde6bfd8460b8e525d122595aedad639d4882fc6723e3dfb86ee09d72024e8`  
		Last Modified: Tue, 18 Nov 2025 10:46:04 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb59777b002fbb9144a4df92f1878f7952c03a391fc95c41a000f07367e6449`  
		Last Modified: Tue, 18 Nov 2025 10:46:05 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cbae22d4c2275e7096343d19b07327bad9a1f2058b7b3233ba160d37c0791be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8c41799de687d9a67018cac858432aa0fef8f73342dd28e1ba390976e351d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:00:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:05:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:05:49 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:49 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 06:17:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:17:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:37 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:17:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151457d95a5866436937e5d27d506481b8563d00b639fb2b4a8c40a19071660b`  
		Last Modified: Tue, 18 Nov 2025 04:01:26 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658d3794cdbd4098e62f50f063ad1c77daee5aa96e3ae3c0720ec13f6f79481`  
		Last Modified: Tue, 18 Nov 2025 04:06:13 GMT  
		Size: 40.9 MB (40939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa13d1b8fcd7d01146fd5b5064fca5a15d13ebfaa4ed43bbb17ad41c9acf21`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56134264619c5f9d99719f23af9471427ea7291468c759595f5c1f1757e7af`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4caacac319447ed5cef1dacae670a1810faa81f77daee3fa4d8849d87316b`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 1.2 MB (1201442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9667cd483d44b60c37d87171e051c983d6916306152a0f527911d7b84a846`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 11.1 MB (11094321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a711a2c6e373b6f1353f031f12e5d703d7703db7940b20eaacfb3097bfbc9c0`  
		Last Modified: Tue, 18 Nov 2025 06:18:35 GMT  
		Size: 118.1 MB (118116320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e854d6b9608165241a45ac9cccd1dbfa3db3bb8173f7ff572ce7f636285f2`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:c39838fb1a8fabc3864e085dc68277ca83d0d360e4528e4dc0d0dfc4d71219ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365c43e8ea0119666083fe9f9d70ce72742706ee55bfbe12d547884e8478d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0f386aace00ef7209fc42e8be14e478d1ae07bfce1215281240047c56d66e6d`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257dba59896dc8affe970c1b9a7a7488b39599bcadcdf8776dbb084ad18d633`  
		Last Modified: Tue, 18 Nov 2025 07:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; s390x

```console
$ docker pull ghost@sha256:f5dc675ba48f5dd47f1746a39a49de73f28a6d8dc0a303cb95017be34b39f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204796779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68050bc4785676a3d0d88a86f7e734771f1c89f72c8853639756a5834f29c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:09:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:13:05 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:13:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:13:14 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:06 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:03:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:35 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d683f4d5080591112b5d19b1b5db2cb7a3d8c47400239407275302d454723f`  
		Last Modified: Tue, 18 Nov 2025 04:10:16 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a3cb3febab65c9bfc8547f93ad9971b384a53c66394ff3a9365a94c74bf19f`  
		Last Modified: Tue, 18 Nov 2025 04:13:43 GMT  
		Size: 41.2 MB (41222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7e39c24509f77776773739aa5bbe814d3e2de93b548ef745ce4bfa44141e9`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 1.7 MB (1712597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2351955604b7ebd37554987c778e617da52b3e8292c6497b1a45243accb6979`  
		Last Modified: Tue, 18 Nov 2025 04:13:39 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee6f822e10fe4fd83989957020a3eca9e0e3ebb7b2e5ad31a9904ec6648714`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 1.2 MB (1221459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fc65be1b596b43240d8b3b08b53fc04f1790dfb7edeaa79b4979e20bae582`  
		Last Modified: Tue, 18 Nov 2025 07:05:24 GMT  
		Size: 11.1 MB (11100261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80eb9144360a07a0c2d8ee8d2780d6f6515f75448e3aab15274b399c213d9`  
		Last Modified: Tue, 18 Nov 2025 07:05:32 GMT  
		Size: 122.7 MB (122651217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226fc85fb3e82ee136221e21f0dfa416f0586db51f30fe20d9915472868dba1`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:36db1953f673e6a4ef29bd80ca3aaefc59f938f541ba4eb3d1a762fa295af3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a7ba99a444e4af864970bfb957e659c7fd89ad91d19c0c124f073dec925d7`

```dockerfile
```

-	Layers:
	-	`sha256:25c88537d8040044f3c95cd023525fcef6b96a5803bbda714520587a236302ec`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702cbca7c5996b9b78c1962b0a85f89383bd30cc0bca27e602c8e2d56c3872a`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-alpine`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-alpine3.22`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.5-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-bookworm`

```console
$ docker pull ghost@sha256:56f66947a25ae319380563bd762f1a68091444e4443c128016ec3e4afb018493
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

### `ghost:5.130.5-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:16d75c50ccf97d39b2a0f6165d96f4bc1d0ca7e9618c679bf66de09693d4d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201286807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f1a5bb3d00c57a30546c5ac92310e230c6784fef54088ddfa65baf15244ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 05:31:20 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:20 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:31:31 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:31:31 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:33 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:33 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:44 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:10:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:10:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:10:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:10:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb6456a5555288c8c6e1aca9b3f6f1b7cf6b913009649e631c6d4134119561`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f691659c2173b66f66f5ecad6e0186f2638e15ecad4a73171e0f70838de5`  
		Last Modified: Tue, 18 Nov 2025 05:31:57 GMT  
		Size: 41.0 MB (40977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c3606ae6509cf726973a0d2f762b7f821b5426849318678222d85ab228f`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eecfc55be5f19d3b0967bb0ae0f53d17786b6a6ca7355d1ca3e9b97f77ca21`  
		Last Modified: Tue, 18 Nov 2025 05:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36b986fb5eb5ed8f7fc039639341f395e63e47f0fbfde03007b249484144d0`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 1.2 MB (1247535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ed7f04cd1e7ac3499a45d0a483cfafa17867d4874f8c1f380161944938b2`  
		Last Modified: Tue, 18 Nov 2025 07:11:34 GMT  
		Size: 11.1 MB (11094625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0af66bf5ab650d8714ccdd11e6a2086d705c82edd02c242460ea8d2d426fac`  
		Last Modified: Tue, 18 Nov 2025 07:11:47 GMT  
		Size: 118.0 MB (118021441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea54a71b860144eea81cfd97d1135a14ca0bbb83dd582ae6557b6930b11dbf`  
		Last Modified: Tue, 18 Nov 2025 07:11:33 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:138aea6a17b263cc6e6c03f54fe42013e7296baba8c0d09b6e6eab085c3cc568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9780c8cac6f79be6aa1a90b51b211a9bfb309b8db040fb7f97867f4acfdd`

```dockerfile
```

-	Layers:
	-	`sha256:dab95cf0370a2401c1e3aad57efaf0740129df26a05de57c000e4848747922e2`  
		Last Modified: Tue, 18 Nov 2025 10:45:58 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180199b9d7d9a2c97d4765664c63152bbc8c83bbefbda4ae8f05dc361ede9ad7`  
		Last Modified: Tue, 18 Nov 2025 10:45:59 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1b4b775e74d10caf91f1bf765826141ae222217a7120f958be4889db0624a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0af20fe06eb7b266bdbdb97e8774edeba1fc0732afc52be23e7c47fcb5331c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:23:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:59 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:41 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:41 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:55 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:29:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527544c5654513868ce4d87aa5d977a07b324ed7c909b8b723f87bb633ed7c6d`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bc82fd181b9997e60069bdef220be82aaf6f3f2b2085d94a3f9dec8b0a013`  
		Last Modified: Tue, 18 Nov 2025 04:24:18 GMT  
		Size: 37.1 MB (37064246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185456839ac256b05beb1e5b4e9a21be6c7f93534d8b9293a2c7759a4e520fc`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de307c97b77fdeaae17f0a556c74372c6872926ec6f33d52b8e7e7642142e7a`  
		Last Modified: Tue, 18 Nov 2025 04:24:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3df8febaf6b4464745efcc043c420cbb59e26e46dfd5d92b47678316dc5bb9`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c22ea2410de9defd76065b35423ca9f81e0a93d0e15e43f57cf102820f958`  
		Last Modified: Tue, 18 Nov 2025 07:30:30 GMT  
		Size: 11.1 MB (11095341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94606ad0102f1fa85b85732ce6811fb461085d590769d0105bde4388cbda7600`  
		Last Modified: Tue, 18 Nov 2025 07:30:45 GMT  
		Size: 120.6 MB (120587361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cdc0ff3787f0b0d0e2784efd40bbbbb74d8301bf9a139c673dee991c2ec5ea`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:18e60ff0419a941f8422caf3fb52687bf2a32462d300662da85a31a510b47da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52791ac377ea7bf1aeb7d7e92be934f93d567079e43f324e58fedc4db47d50`

```dockerfile
```

-	Layers:
	-	`sha256:0adde6bfd8460b8e525d122595aedad639d4882fc6723e3dfb86ee09d72024e8`  
		Last Modified: Tue, 18 Nov 2025 10:46:04 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb59777b002fbb9144a4df92f1878f7952c03a391fc95c41a000f07367e6449`  
		Last Modified: Tue, 18 Nov 2025 10:46:05 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cbae22d4c2275e7096343d19b07327bad9a1f2058b7b3233ba160d37c0791be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8c41799de687d9a67018cac858432aa0fef8f73342dd28e1ba390976e351d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:00:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:05:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:37 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:05:49 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:49 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:16:11 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:23 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 06:17:36 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:17:37 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:37 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:17:37 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151457d95a5866436937e5d27d506481b8563d00b639fb2b4a8c40a19071660b`  
		Last Modified: Tue, 18 Nov 2025 04:01:26 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658d3794cdbd4098e62f50f063ad1c77daee5aa96e3ae3c0720ec13f6f79481`  
		Last Modified: Tue, 18 Nov 2025 04:06:13 GMT  
		Size: 40.9 MB (40939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa13d1b8fcd7d01146fd5b5064fca5a15d13ebfaa4ed43bbb17ad41c9acf21`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 1.7 MB (1712606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56134264619c5f9d99719f23af9471427ea7291468c759595f5c1f1757e7af`  
		Last Modified: Tue, 18 Nov 2025 04:06:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4caacac319447ed5cef1dacae670a1810faa81f77daee3fa4d8849d87316b`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 1.2 MB (1201442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9667cd483d44b60c37d87171e051c983d6916306152a0f527911d7b84a846`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 11.1 MB (11094321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a711a2c6e373b6f1353f031f12e5d703d7703db7940b20eaacfb3097bfbc9c0`  
		Last Modified: Tue, 18 Nov 2025 06:18:35 GMT  
		Size: 118.1 MB (118116320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e854d6b9608165241a45ac9cccd1dbfa3db3bb8173f7ff572ce7f636285f2`  
		Last Modified: Tue, 18 Nov 2025 06:18:22 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c39838fb1a8fabc3864e085dc68277ca83d0d360e4528e4dc0d0dfc4d71219ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365c43e8ea0119666083fe9f9d70ce72742706ee55bfbe12d547884e8478d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0f386aace00ef7209fc42e8be14e478d1ae07bfce1215281240047c56d66e6d`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257dba59896dc8affe970c1b9a7a7488b39599bcadcdf8776dbb084ad18d633`  
		Last Modified: Tue, 18 Nov 2025 07:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:f5dc675ba48f5dd47f1746a39a49de73f28a6d8dc0a303cb95017be34b39f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204796779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68050bc4785676a3d0d88a86f7e734771f1c89f72c8853639756a5834f29c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:09:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV NODE_VERSION=20.19.5
# Tue, 18 Nov 2025 04:13:05 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:05 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:13:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:13:14 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:06 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:06 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 18 Nov 2025 07:03:33 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:34 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:35 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d683f4d5080591112b5d19b1b5db2cb7a3d8c47400239407275302d454723f`  
		Last Modified: Tue, 18 Nov 2025 04:10:16 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a3cb3febab65c9bfc8547f93ad9971b384a53c66394ff3a9365a94c74bf19f`  
		Last Modified: Tue, 18 Nov 2025 04:13:43 GMT  
		Size: 41.2 MB (41222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7e39c24509f77776773739aa5bbe814d3e2de93b548ef745ce4bfa44141e9`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 1.7 MB (1712597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2351955604b7ebd37554987c778e617da52b3e8292c6497b1a45243accb6979`  
		Last Modified: Tue, 18 Nov 2025 04:13:39 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee6f822e10fe4fd83989957020a3eca9e0e3ebb7b2e5ad31a9904ec6648714`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 1.2 MB (1221459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fc65be1b596b43240d8b3b08b53fc04f1790dfb7edeaa79b4979e20bae582`  
		Last Modified: Tue, 18 Nov 2025 07:05:24 GMT  
		Size: 11.1 MB (11100261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80eb9144360a07a0c2d8ee8d2780d6f6515f75448e3aab15274b399c213d9`  
		Last Modified: Tue, 18 Nov 2025 07:05:32 GMT  
		Size: 122.7 MB (122651217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226fc85fb3e82ee136221e21f0dfa416f0586db51f30fe20d9915472868dba1`  
		Last Modified: Tue, 18 Nov 2025 07:05:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:36db1953f673e6a4ef29bd80ca3aaefc59f938f541ba4eb3d1a762fa295af3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a7ba99a444e4af864970bfb957e659c7fd89ad91d19c0c124f073dec925d7`

```dockerfile
```

-	Layers:
	-	`sha256:25c88537d8040044f3c95cd023525fcef6b96a5803bbda714520587a236302ec`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702cbca7c5996b9b78c1962b0a85f89383bd30cc0bca27e602c8e2d56c3872a`  
		Last Modified: Tue, 18 Nov 2025 07:46:35 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6`

```console
$ docker pull ghost@sha256:0c70f4153a05e875c046bf2a763ecd1d47ff403ba2b35c3af5a3fcbe76ded772
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
$ docker pull ghost@sha256:fd792d31faf9c72ce1132b43732e3b996afc010bcd67fd7e1769a8a5e21ea83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220015950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e76b55d62ee5f57a2f2629587dae1b49d039b851cfd02aa24a8b884778f14b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:26:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 05:29:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:29:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:29:58 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:00 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:11:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:11:24 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:24 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:11:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942578950a9229a852f0de33e4e5ff14a882d26d1ca25de0d239c09ae1a3271b`  
		Last Modified: Tue, 18 Nov 2025 05:27:35 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e6aad59bf1a2f3111ba30aeba5544b0a5379113ea4cc61f8bbf1acfb442dba`  
		Last Modified: Tue, 18 Nov 2025 05:30:22 GMT  
		Size: 49.5 MB (49481526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f7d23d4cdc8c290c919165cf1a555f4d5197ee7046c0429ae5de36bb3fda3`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419608b38e593ad78de784c2b22c7f3ae8d1ba15dbf8dbe3fabeffa3c27419e`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b056b2197ec736f8cf7d1b5887359b81357b2690f31b41d6a5155ad80f7e6398`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 1.2 MB (1247533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759e78cde27ef7836641c7142a7b88209d66c23975a490fc46732a70f9e7d44`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 11.7 MB (11663639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d2b2ac02b40714cc61f7c2f937f590709ee929c9954446f2ae6b3a12d7914`  
		Last Modified: Tue, 18 Nov 2025 07:12:24 GMT  
		Size: 127.7 MB (127677853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc938c3386ad45611101bef76a38a4bf1f712d9860dd254474e8e7c4b7e4bb6`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:3769437c228cc33bd6f6314944b2e33911dbde5d7f1a3eb4e3b6168af01c4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd9ec508f22d54d19243d894a399e7e34ca0edbca7371a59dee24128afbf136`

```dockerfile
```

-	Layers:
	-	`sha256:26893031743eec8901db1bc6c96b5e1929b55ee0d486add4de745550f403c12d`  
		Last Modified: Tue, 18 Nov 2025 10:46:21 GMT  
		Size: 5.6 MB (5610688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcd49853fa4834880a3f1e656a1f7b1954facb85a8a45fa9db8b1522912b701`  
		Last Modified: Tue, 18 Nov 2025 10:46:22 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:995cd65fa2aca91e83eda3c71ce1a5461bd7a49e7a1935709399ebccd7c561fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a05ab353924aacdfdbef47cf48d7514682ec29306f87753a44d82f116cd4b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:23:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:51 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:32 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:29:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:43 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:43 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0647d91c59ce8c8d984e0d8a464ae67e3d18cfba6e102b4b9df3d23ace254886`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aec5cbb97a45b1295e632f50a486c86084369aba94dcb9baaa4b2f589a919d`  
		Last Modified: Tue, 18 Nov 2025 04:24:13 GMT  
		Size: 44.2 MB (44208140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f8dd114fc0077d2ef22d4e7ad09dfb945a9b18a58e75b6f237ee4f59717128`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 1.7 MB (1712780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f611703056a722d286e4abea947d6f7a29129d37ff2a28dd02acd739d1e7a117`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7a6a6416d331bfe046423b73e51e0d89e36462eb2f3a188c96d27790d3f5c`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb7ce7a5a3dfdbd679fce04e3d38f147d35993f0a57a64124074dd94c987d3`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 11.7 MB (11660200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0061525f729d8f190bd0bdd8299b65cb3f62c7faf5afa8d39ecfc8ec65e41ab`  
		Last Modified: Tue, 18 Nov 2025 11:23:42 GMT  
		Size: 128.7 MB (128736935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d24192eb8d1f6db02dee05b0e3170dc7dade4de7ce93f4884601941bda9c0b`  
		Last Modified: Tue, 18 Nov 2025 07:30:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:756bd77b45dcb6d61c042d770075e103fd51c6586116befc831c5da9b223e907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce12acf64e85084b7377e248875df8d50c73ba6aa09a3d0ffca6bee6b78fe1fb`

```dockerfile
```

-	Layers:
	-	`sha256:0aee169b1ffcc2e456f4bc5da786961494f1a149dc121d484a6c1773de9be757`  
		Last Modified: Tue, 18 Nov 2025 10:46:26 GMT  
		Size: 5.6 MB (5613487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0cff61496ff7e4381947023547bc08fa851c8aa79348e8ea0babc1a599e6fc`  
		Last Modified: Tue, 18 Nov 2025 10:46:27 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:258c4407d6d7bce9f9eef454ae918168b9905ae91fad8e2c6784d3eed4819cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220074205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8399decb593f9e243b712665934c16a889eae908e7e077dc1a77f256824c57bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:03:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:03:44 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:44 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:15:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:15:49 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:17 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 06:18:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:18:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:18:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e88625ec434b2584983383ce17b9544a3c599a885f7dcd0ca01d5804a1eec3a`  
		Last Modified: Tue, 18 Nov 2025 03:58:47 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26974ee5c741410e72a5aaeeee45d4377f5d2c1a52f3a56c09a97bb8abce5f`  
		Last Modified: Tue, 18 Nov 2025 04:04:11 GMT  
		Size: 49.6 MB (49614746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393386629f425518f5340811baae8dc86203636e0049338341c222e66e3057ef`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26540316edc055fdeb9b9eebee982d07ce412a09a722e07f64f64bd398cdfced`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715eee0464cfc96ba6c1b685fb3f359b828a0c7e7d2b8be0222d5d5544c484c7`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 1.2 MB (1201406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8035a91ebbd314903564682e0e427992e79d7a14fb0eafad2c71e4a002f573`  
		Last Modified: Tue, 18 Nov 2025 06:19:33 GMT  
		Size: 11.7 MB (11666371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980312c520ebcbad91e097ac0916660d49c7b05de98f424f6151f0b9917300e7`  
		Last Modified: Tue, 18 Nov 2025 06:19:41 GMT  
		Size: 127.8 MB (127772562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083639d9f6e238da2de3217eba8c3ada171926da1a0866fff6206396526bff59`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:cc9b52228daba5c3e2f262152adb0efa70f07d276b8ffc6db69d60df2a9c169e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7606ad196d35ba7f0d10c58e0ae40aab5321270a3e7435031ba435b0ae49fe`

```dockerfile
```

-	Layers:
	-	`sha256:b848dd81ea7646f37749d26fc92914936bf8af1ef6b71e659ad53df002a56dc2`  
		Last Modified: Tue, 18 Nov 2025 07:46:51 GMT  
		Size: 5.6 MB (5611039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b84ad264e41bccd5cfc9d153f75624e06803a68097e7c909ff538218ae37d9`  
		Last Modified: Tue, 18 Nov 2025 07:46:52 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:c3f1e7ead6676aa1584be14ebf9d9b4550b6bc1bbe396ed49bdf5e77de7eace3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3452894f8734c3d058ea4cb0278c7d8fa1cb40be4b6125260abd4f095a18980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:11:39 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:11:55 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:12:04 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:12:04 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:04 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:03:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:45 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:45 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:46 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499a8c640bba2d2c845b32a54d35f79f91741fefd38b97e1da3f71e752be2382`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31a3dad6a431bde6ec5161ea2c1432c62d82552cf9303600f3e2746dcd4ee`  
		Last Modified: Tue, 18 Nov 2025 04:12:41 GMT  
		Size: 49.7 MB (49676885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b22afc160ee4d6820ca8130d8a93d583df65df36055faf0e8e553aaf57bb6ff`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf53011c4bc2010e35980a5a682d5882000d36c5b385c845afd82173abd258e`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f8ef58685220dfe83dd97c2b3dcea755e6c7049e6231fd97aa8a3133c94a72`  
		Last Modified: Tue, 18 Nov 2025 07:05:39 GMT  
		Size: 1.2 MB (1221443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cb90fd75a53807b356490ca5520a75993c61c5f320395a463fb2f245bdf055`  
		Last Modified: Tue, 18 Nov 2025 07:05:40 GMT  
		Size: 11.7 MB (11682323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fea2233ae68d7080525c5311d18fc2f141032987f0a6e4cecc6bf5ebbaa4b0`  
		Last Modified: Tue, 18 Nov 2025 10:08:27 GMT  
		Size: 130.8 MB (130810057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26afe088044265f6245c4c21b84d4fdf063cb1b784fb14a98eaa4cedce49aac`  
		Last Modified: Tue, 18 Nov 2025 07:05:38 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:e5e321b7cf2edae165e31379ee8b70220005b0a967950527a781ed57d459276a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4febf40b76ebf8f90523a5585f55fe64a8fcad6666bb8c4401d39082d745de1a`

```dockerfile
```

-	Layers:
	-	`sha256:63284f20b241d705bc393f6fa2f4a5fa5835d07e057507c4aacc98450713b979`  
		Last Modified: Tue, 18 Nov 2025 07:46:57 GMT  
		Size: 5.6 MB (5604515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c087b81d1871251fef1c8126ce47429ffbd371565c5030a4595d4af5df7ad4be`  
		Last Modified: Tue, 18 Nov 2025 07:46:58 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:099877e737b34c4ffee73d175bf958fc58327222f40164b4e752f37be198019f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:9cf69af4186b92c30cf812015e4fb21c12efe08fb5d4024320d229323b9129c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197474158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66838b635a1a3ad976df1d9d9bde90e60e44e9162578982e82d447e7bbc8e4c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Tue, 18 Nov 2025 02:58:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:58:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 02:58:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 03:01:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 03:01:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 03:01:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:01:02 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 03:01:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64991591e6b40e1c3c06160b49831ea44d8ae239db386d2c8f043f1f4683543a`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 777.0 KB (777043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a57d492c5c1f8987cef7b043f16a77b42869cf100e0d15347ffbf02523c5a7`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 923.4 KB (923437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8f19a3f750a6da635c75659076651f228e42d6c3c9908da981dac52caba87`  
		Last Modified: Tue, 18 Nov 2025 03:01:45 GMT  
		Size: 11.7 MB (11664128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c8087c26299eb568ef1d30846eb83f8090d38c290b719c065d70cc5ddf5ee9`  
		Last Modified: Tue, 18 Nov 2025 03:01:58 GMT  
		Size: 127.5 MB (127478488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e226addc3f115d463f01fc2d5994c3620c4436777a07d0c612d55bc709ac251`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:fb075ce145607812a9b6bd343a14735644fc04071f86277b36d2043475d3ff2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442a0962dd0be6e8ff507d7c6d019e4abb3d154ee83f1f80a6e3aaad5688acac`

```dockerfile
```

-	Layers:
	-	`sha256:148e7805d13e7f0a46f2d53abb7c59a77c7bea3bbe057b8c202ab18f432d9f7c`  
		Last Modified: Tue, 18 Nov 2025 04:47:09 GMT  
		Size: 3.4 MB (3397590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6632c6061cbe0a7ccf80e7e3d66fff2ad5b8e6f1dae08e595fa4776cff3c9987`  
		Last Modified: Tue, 18 Nov 2025 04:47:10 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2d1a3f0d74b2bc6139c10582f2d7f32a9c4b25f4dc660a297ddfbbb286265ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208334511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1621b319c46c07576a3684bb1cf1064cca7f316e7b26a59f84219e186c93d02a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Mon, 17 Nov 2025 23:31:23 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GOSU_VERSION=1.19
# Mon, 17 Nov 2025 23:31:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV NODE_ENV=production
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 17 Nov 2025 23:31:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_VERSION=6.8.1
# Mon, 17 Nov 2025 23:34:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
WORKDIR /var/lib/ghost
# Mon, 17 Nov 2025 23:34:30 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 17 Nov 2025 23:34:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:34:30 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 17 Nov 2025 23:34:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1827a5c4524186118eee00a4ac63d63193f596b938559b665bc04324b9ad1f`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ee73bf02cc21d58721e5860fb78e417016e95199c7ae7200ae0bda2dbf2c7`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 876.4 KB (876367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d64b7446ae5dc06d711f1426ee8b76d3347a12a6d4cc5e6d7d7ae1761303bf`  
		Last Modified: Mon, 17 Nov 2025 23:35:18 GMT  
		Size: 11.7 MB (11667754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5d1df407927fc4fbb55e170799a247fa44e76425b5ff769e66d933373a4e6`  
		Last Modified: Tue, 18 Nov 2025 01:46:15 GMT  
		Size: 138.3 MB (138275091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4cc7c18b66830086b72324d1b2c0364f34d7957eecf34ca1dc59641b9c2ed`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4ccf5fb9eaf7257f301bde1e1b23cedc1a75d066833c8d112c1c54bcff537ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade1dc922fe906e118c634045e294e4e4f5291540c9139ecf4e0e840661d059`

```dockerfile
```

-	Layers:
	-	`sha256:95ee7b85f3cdd1151d26ba89ad27a6c99e15d81e1a1c4ee8caf308c16d0384c6`  
		Last Modified: Tue, 18 Nov 2025 01:45:40 GMT  
		Size: 3.4 MB (3397746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074563961effd80c19f806f12fa2242710f6c81daf01ea409984a48be72be4cd`  
		Last Modified: Tue, 18 Nov 2025 01:45:41 GMT  
		Size: 26.6 KB (26572 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.22`

```console
$ docker pull ghost@sha256:099877e737b34c4ffee73d175bf958fc58327222f40164b4e752f37be198019f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:9cf69af4186b92c30cf812015e4fb21c12efe08fb5d4024320d229323b9129c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197474158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66838b635a1a3ad976df1d9d9bde90e60e44e9162578982e82d447e7bbc8e4c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Tue, 18 Nov 2025 02:58:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:58:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 02:58:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 03:01:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 03:01:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 03:01:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:01:02 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 03:01:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64991591e6b40e1c3c06160b49831ea44d8ae239db386d2c8f043f1f4683543a`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 777.0 KB (777043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a57d492c5c1f8987cef7b043f16a77b42869cf100e0d15347ffbf02523c5a7`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 923.4 KB (923437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8f19a3f750a6da635c75659076651f228e42d6c3c9908da981dac52caba87`  
		Last Modified: Tue, 18 Nov 2025 03:01:45 GMT  
		Size: 11.7 MB (11664128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c8087c26299eb568ef1d30846eb83f8090d38c290b719c065d70cc5ddf5ee9`  
		Last Modified: Tue, 18 Nov 2025 03:01:58 GMT  
		Size: 127.5 MB (127478488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e226addc3f115d463f01fc2d5994c3620c4436777a07d0c612d55bc709ac251`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:fb075ce145607812a9b6bd343a14735644fc04071f86277b36d2043475d3ff2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442a0962dd0be6e8ff507d7c6d019e4abb3d154ee83f1f80a6e3aaad5688acac`

```dockerfile
```

-	Layers:
	-	`sha256:148e7805d13e7f0a46f2d53abb7c59a77c7bea3bbe057b8c202ab18f432d9f7c`  
		Last Modified: Tue, 18 Nov 2025 04:47:09 GMT  
		Size: 3.4 MB (3397590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6632c6061cbe0a7ccf80e7e3d66fff2ad5b8e6f1dae08e595fa4776cff3c9987`  
		Last Modified: Tue, 18 Nov 2025 04:47:10 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2d1a3f0d74b2bc6139c10582f2d7f32a9c4b25f4dc660a297ddfbbb286265ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208334511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1621b319c46c07576a3684bb1cf1064cca7f316e7b26a59f84219e186c93d02a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Mon, 17 Nov 2025 23:31:23 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GOSU_VERSION=1.19
# Mon, 17 Nov 2025 23:31:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV NODE_ENV=production
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 17 Nov 2025 23:31:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_VERSION=6.8.1
# Mon, 17 Nov 2025 23:34:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
WORKDIR /var/lib/ghost
# Mon, 17 Nov 2025 23:34:30 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 17 Nov 2025 23:34:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:34:30 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 17 Nov 2025 23:34:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1827a5c4524186118eee00a4ac63d63193f596b938559b665bc04324b9ad1f`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ee73bf02cc21d58721e5860fb78e417016e95199c7ae7200ae0bda2dbf2c7`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 876.4 KB (876367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d64b7446ae5dc06d711f1426ee8b76d3347a12a6d4cc5e6d7d7ae1761303bf`  
		Last Modified: Mon, 17 Nov 2025 23:35:18 GMT  
		Size: 11.7 MB (11667754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5d1df407927fc4fbb55e170799a247fa44e76425b5ff769e66d933373a4e6`  
		Last Modified: Tue, 18 Nov 2025 01:46:15 GMT  
		Size: 138.3 MB (138275091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4cc7c18b66830086b72324d1b2c0364f34d7957eecf34ca1dc59641b9c2ed`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:4ccf5fb9eaf7257f301bde1e1b23cedc1a75d066833c8d112c1c54bcff537ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade1dc922fe906e118c634045e294e4e4f5291540c9139ecf4e0e840661d059`

```dockerfile
```

-	Layers:
	-	`sha256:95ee7b85f3cdd1151d26ba89ad27a6c99e15d81e1a1c4ee8caf308c16d0384c6`  
		Last Modified: Tue, 18 Nov 2025 01:45:40 GMT  
		Size: 3.4 MB (3397746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074563961effd80c19f806f12fa2242710f6c81daf01ea409984a48be72be4cd`  
		Last Modified: Tue, 18 Nov 2025 01:45:41 GMT  
		Size: 26.6 KB (26572 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:0c70f4153a05e875c046bf2a763ecd1d47ff403ba2b35c3af5a3fcbe76ded772
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
$ docker pull ghost@sha256:fd792d31faf9c72ce1132b43732e3b996afc010bcd67fd7e1769a8a5e21ea83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220015950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e76b55d62ee5f57a2f2629587dae1b49d039b851cfd02aa24a8b884778f14b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:26:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 05:29:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:29:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:29:58 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:00 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:11:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:11:24 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:24 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:11:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942578950a9229a852f0de33e4e5ff14a882d26d1ca25de0d239c09ae1a3271b`  
		Last Modified: Tue, 18 Nov 2025 05:27:35 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e6aad59bf1a2f3111ba30aeba5544b0a5379113ea4cc61f8bbf1acfb442dba`  
		Last Modified: Tue, 18 Nov 2025 05:30:22 GMT  
		Size: 49.5 MB (49481526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f7d23d4cdc8c290c919165cf1a555f4d5197ee7046c0429ae5de36bb3fda3`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419608b38e593ad78de784c2b22c7f3ae8d1ba15dbf8dbe3fabeffa3c27419e`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b056b2197ec736f8cf7d1b5887359b81357b2690f31b41d6a5155ad80f7e6398`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 1.2 MB (1247533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759e78cde27ef7836641c7142a7b88209d66c23975a490fc46732a70f9e7d44`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 11.7 MB (11663639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d2b2ac02b40714cc61f7c2f937f590709ee929c9954446f2ae6b3a12d7914`  
		Last Modified: Tue, 18 Nov 2025 07:12:24 GMT  
		Size: 127.7 MB (127677853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc938c3386ad45611101bef76a38a4bf1f712d9860dd254474e8e7c4b7e4bb6`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:3769437c228cc33bd6f6314944b2e33911dbde5d7f1a3eb4e3b6168af01c4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd9ec508f22d54d19243d894a399e7e34ca0edbca7371a59dee24128afbf136`

```dockerfile
```

-	Layers:
	-	`sha256:26893031743eec8901db1bc6c96b5e1929b55ee0d486add4de745550f403c12d`  
		Last Modified: Tue, 18 Nov 2025 10:46:21 GMT  
		Size: 5.6 MB (5610688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcd49853fa4834880a3f1e656a1f7b1954facb85a8a45fa9db8b1522912b701`  
		Last Modified: Tue, 18 Nov 2025 10:46:22 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:995cd65fa2aca91e83eda3c71ce1a5461bd7a49e7a1935709399ebccd7c561fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a05ab353924aacdfdbef47cf48d7514682ec29306f87753a44d82f116cd4b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:23:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:51 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:32 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:29:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:43 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:43 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0647d91c59ce8c8d984e0d8a464ae67e3d18cfba6e102b4b9df3d23ace254886`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aec5cbb97a45b1295e632f50a486c86084369aba94dcb9baaa4b2f589a919d`  
		Last Modified: Tue, 18 Nov 2025 04:24:13 GMT  
		Size: 44.2 MB (44208140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f8dd114fc0077d2ef22d4e7ad09dfb945a9b18a58e75b6f237ee4f59717128`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 1.7 MB (1712780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f611703056a722d286e4abea947d6f7a29129d37ff2a28dd02acd739d1e7a117`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7a6a6416d331bfe046423b73e51e0d89e36462eb2f3a188c96d27790d3f5c`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb7ce7a5a3dfdbd679fce04e3d38f147d35993f0a57a64124074dd94c987d3`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 11.7 MB (11660200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0061525f729d8f190bd0bdd8299b65cb3f62c7faf5afa8d39ecfc8ec65e41ab`  
		Last Modified: Tue, 18 Nov 2025 11:23:42 GMT  
		Size: 128.7 MB (128736935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d24192eb8d1f6db02dee05b0e3170dc7dade4de7ce93f4884601941bda9c0b`  
		Last Modified: Tue, 18 Nov 2025 07:30:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:756bd77b45dcb6d61c042d770075e103fd51c6586116befc831c5da9b223e907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce12acf64e85084b7377e248875df8d50c73ba6aa09a3d0ffca6bee6b78fe1fb`

```dockerfile
```

-	Layers:
	-	`sha256:0aee169b1ffcc2e456f4bc5da786961494f1a149dc121d484a6c1773de9be757`  
		Last Modified: Tue, 18 Nov 2025 10:46:26 GMT  
		Size: 5.6 MB (5613487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0cff61496ff7e4381947023547bc08fa851c8aa79348e8ea0babc1a599e6fc`  
		Last Modified: Tue, 18 Nov 2025 10:46:27 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:258c4407d6d7bce9f9eef454ae918168b9905ae91fad8e2c6784d3eed4819cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220074205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8399decb593f9e243b712665934c16a889eae908e7e077dc1a77f256824c57bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:03:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:03:44 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:44 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:15:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:15:49 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:17 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 06:18:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:18:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:18:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e88625ec434b2584983383ce17b9544a3c599a885f7dcd0ca01d5804a1eec3a`  
		Last Modified: Tue, 18 Nov 2025 03:58:47 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26974ee5c741410e72a5aaeeee45d4377f5d2c1a52f3a56c09a97bb8abce5f`  
		Last Modified: Tue, 18 Nov 2025 04:04:11 GMT  
		Size: 49.6 MB (49614746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393386629f425518f5340811baae8dc86203636e0049338341c222e66e3057ef`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26540316edc055fdeb9b9eebee982d07ce412a09a722e07f64f64bd398cdfced`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715eee0464cfc96ba6c1b685fb3f359b828a0c7e7d2b8be0222d5d5544c484c7`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 1.2 MB (1201406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8035a91ebbd314903564682e0e427992e79d7a14fb0eafad2c71e4a002f573`  
		Last Modified: Tue, 18 Nov 2025 06:19:33 GMT  
		Size: 11.7 MB (11666371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980312c520ebcbad91e097ac0916660d49c7b05de98f424f6151f0b9917300e7`  
		Last Modified: Tue, 18 Nov 2025 06:19:41 GMT  
		Size: 127.8 MB (127772562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083639d9f6e238da2de3217eba8c3ada171926da1a0866fff6206396526bff59`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:cc9b52228daba5c3e2f262152adb0efa70f07d276b8ffc6db69d60df2a9c169e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7606ad196d35ba7f0d10c58e0ae40aab5321270a3e7435031ba435b0ae49fe`

```dockerfile
```

-	Layers:
	-	`sha256:b848dd81ea7646f37749d26fc92914936bf8af1ef6b71e659ad53df002a56dc2`  
		Last Modified: Tue, 18 Nov 2025 07:46:51 GMT  
		Size: 5.6 MB (5611039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b84ad264e41bccd5cfc9d153f75624e06803a68097e7c909ff538218ae37d9`  
		Last Modified: Tue, 18 Nov 2025 07:46:52 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c3f1e7ead6676aa1584be14ebf9d9b4550b6bc1bbe396ed49bdf5e77de7eace3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3452894f8734c3d058ea4cb0278c7d8fa1cb40be4b6125260abd4f095a18980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:11:39 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:11:55 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:12:04 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:12:04 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:04 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:03:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:45 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:45 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:46 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499a8c640bba2d2c845b32a54d35f79f91741fefd38b97e1da3f71e752be2382`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31a3dad6a431bde6ec5161ea2c1432c62d82552cf9303600f3e2746dcd4ee`  
		Last Modified: Tue, 18 Nov 2025 04:12:41 GMT  
		Size: 49.7 MB (49676885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b22afc160ee4d6820ca8130d8a93d583df65df36055faf0e8e553aaf57bb6ff`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf53011c4bc2010e35980a5a682d5882000d36c5b385c845afd82173abd258e`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f8ef58685220dfe83dd97c2b3dcea755e6c7049e6231fd97aa8a3133c94a72`  
		Last Modified: Tue, 18 Nov 2025 07:05:39 GMT  
		Size: 1.2 MB (1221443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cb90fd75a53807b356490ca5520a75993c61c5f320395a463fb2f245bdf055`  
		Last Modified: Tue, 18 Nov 2025 07:05:40 GMT  
		Size: 11.7 MB (11682323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fea2233ae68d7080525c5311d18fc2f141032987f0a6e4cecc6bf5ebbaa4b0`  
		Last Modified: Tue, 18 Nov 2025 10:08:27 GMT  
		Size: 130.8 MB (130810057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26afe088044265f6245c4c21b84d4fdf063cb1b784fb14a98eaa4cedce49aac`  
		Last Modified: Tue, 18 Nov 2025 07:05:38 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:e5e321b7cf2edae165e31379ee8b70220005b0a967950527a781ed57d459276a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4febf40b76ebf8f90523a5585f55fe64a8fcad6666bb8c4401d39082d745de1a`

```dockerfile
```

-	Layers:
	-	`sha256:63284f20b241d705bc393f6fa2f4a5fa5835d07e057507c4aacc98450713b979`  
		Last Modified: Tue, 18 Nov 2025 07:46:57 GMT  
		Size: 5.6 MB (5604515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c087b81d1871251fef1c8126ce47429ffbd371565c5030a4595d4af5df7ad4be`  
		Last Modified: Tue, 18 Nov 2025 07:46:58 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.9`

**does not exist** (yet?)

## `ghost:6.9-alpine`

**does not exist** (yet?)

## `ghost:6.9-alpine3.22`

**does not exist** (yet?)

## `ghost:6.9-bookworm`

**does not exist** (yet?)

## `ghost:6.9.0`

**does not exist** (yet?)

## `ghost:6.9.0-alpine`

**does not exist** (yet?)

## `ghost:6.9.0-alpine3.22`

**does not exist** (yet?)

## `ghost:6.9.0-bookworm`

**does not exist** (yet?)

## `ghost:alpine`

```console
$ docker pull ghost@sha256:099877e737b34c4ffee73d175bf958fc58327222f40164b4e752f37be198019f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:9cf69af4186b92c30cf812015e4fb21c12efe08fb5d4024320d229323b9129c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197474158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66838b635a1a3ad976df1d9d9bde90e60e44e9162578982e82d447e7bbc8e4c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Tue, 18 Nov 2025 02:58:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:58:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 02:58:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 03:01:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 03:01:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 03:01:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:01:02 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 03:01:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64991591e6b40e1c3c06160b49831ea44d8ae239db386d2c8f043f1f4683543a`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 777.0 KB (777043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a57d492c5c1f8987cef7b043f16a77b42869cf100e0d15347ffbf02523c5a7`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 923.4 KB (923437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8f19a3f750a6da635c75659076651f228e42d6c3c9908da981dac52caba87`  
		Last Modified: Tue, 18 Nov 2025 03:01:45 GMT  
		Size: 11.7 MB (11664128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c8087c26299eb568ef1d30846eb83f8090d38c290b719c065d70cc5ddf5ee9`  
		Last Modified: Tue, 18 Nov 2025 03:01:58 GMT  
		Size: 127.5 MB (127478488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e226addc3f115d463f01fc2d5994c3620c4436777a07d0c612d55bc709ac251`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:fb075ce145607812a9b6bd343a14735644fc04071f86277b36d2043475d3ff2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442a0962dd0be6e8ff507d7c6d019e4abb3d154ee83f1f80a6e3aaad5688acac`

```dockerfile
```

-	Layers:
	-	`sha256:148e7805d13e7f0a46f2d53abb7c59a77c7bea3bbe057b8c202ab18f432d9f7c`  
		Last Modified: Tue, 18 Nov 2025 04:47:09 GMT  
		Size: 3.4 MB (3397590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6632c6061cbe0a7ccf80e7e3d66fff2ad5b8e6f1dae08e595fa4776cff3c9987`  
		Last Modified: Tue, 18 Nov 2025 04:47:10 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2d1a3f0d74b2bc6139c10582f2d7f32a9c4b25f4dc660a297ddfbbb286265ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208334511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1621b319c46c07576a3684bb1cf1064cca7f316e7b26a59f84219e186c93d02a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Mon, 17 Nov 2025 23:31:23 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GOSU_VERSION=1.19
# Mon, 17 Nov 2025 23:31:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV NODE_ENV=production
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 17 Nov 2025 23:31:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_VERSION=6.8.1
# Mon, 17 Nov 2025 23:34:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
WORKDIR /var/lib/ghost
# Mon, 17 Nov 2025 23:34:30 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 17 Nov 2025 23:34:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:34:30 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 17 Nov 2025 23:34:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1827a5c4524186118eee00a4ac63d63193f596b938559b665bc04324b9ad1f`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ee73bf02cc21d58721e5860fb78e417016e95199c7ae7200ae0bda2dbf2c7`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 876.4 KB (876367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d64b7446ae5dc06d711f1426ee8b76d3347a12a6d4cc5e6d7d7ae1761303bf`  
		Last Modified: Mon, 17 Nov 2025 23:35:18 GMT  
		Size: 11.7 MB (11667754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5d1df407927fc4fbb55e170799a247fa44e76425b5ff769e66d933373a4e6`  
		Last Modified: Tue, 18 Nov 2025 01:46:15 GMT  
		Size: 138.3 MB (138275091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4cc7c18b66830086b72324d1b2c0364f34d7957eecf34ca1dc59641b9c2ed`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:4ccf5fb9eaf7257f301bde1e1b23cedc1a75d066833c8d112c1c54bcff537ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade1dc922fe906e118c634045e294e4e4f5291540c9139ecf4e0e840661d059`

```dockerfile
```

-	Layers:
	-	`sha256:95ee7b85f3cdd1151d26ba89ad27a6c99e15d81e1a1c4ee8caf308c16d0384c6`  
		Last Modified: Tue, 18 Nov 2025 01:45:40 GMT  
		Size: 3.4 MB (3397746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074563961effd80c19f806f12fa2242710f6c81daf01ea409984a48be72be4cd`  
		Last Modified: Tue, 18 Nov 2025 01:45:41 GMT  
		Size: 26.6 KB (26572 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.22`

```console
$ docker pull ghost@sha256:099877e737b34c4ffee73d175bf958fc58327222f40164b4e752f37be198019f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:9cf69af4186b92c30cf812015e4fb21c12efe08fb5d4024320d229323b9129c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197474158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66838b635a1a3ad976df1d9d9bde90e60e44e9162578982e82d447e7bbc8e4c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Tue, 18 Nov 2025 02:58:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:58:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:58:15 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 02:58:15 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 02:58:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 02:58:36 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 03:01:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 03:01:02 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 03:01:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:01:02 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 03:01:02 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64991591e6b40e1c3c06160b49831ea44d8ae239db386d2c8f043f1f4683543a`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 777.0 KB (777043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a57d492c5c1f8987cef7b043f16a77b42869cf100e0d15347ffbf02523c5a7`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 923.4 KB (923437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8f19a3f750a6da635c75659076651f228e42d6c3c9908da981dac52caba87`  
		Last Modified: Tue, 18 Nov 2025 03:01:45 GMT  
		Size: 11.7 MB (11664128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c8087c26299eb568ef1d30846eb83f8090d38c290b719c065d70cc5ddf5ee9`  
		Last Modified: Tue, 18 Nov 2025 03:01:58 GMT  
		Size: 127.5 MB (127478488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e226addc3f115d463f01fc2d5994c3620c4436777a07d0c612d55bc709ac251`  
		Last Modified: Tue, 18 Nov 2025 03:01:44 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:fb075ce145607812a9b6bd343a14735644fc04071f86277b36d2043475d3ff2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442a0962dd0be6e8ff507d7c6d019e4abb3d154ee83f1f80a6e3aaad5688acac`

```dockerfile
```

-	Layers:
	-	`sha256:148e7805d13e7f0a46f2d53abb7c59a77c7bea3bbe057b8c202ab18f432d9f7c`  
		Last Modified: Tue, 18 Nov 2025 04:47:09 GMT  
		Size: 3.4 MB (3397590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6632c6061cbe0a7ccf80e7e3d66fff2ad5b8e6f1dae08e595fa4776cff3c9987`  
		Last Modified: Tue, 18 Nov 2025 04:47:10 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2d1a3f0d74b2bc6139c10582f2d7f32a9c4b25f4dc660a297ddfbbb286265ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208334511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1621b319c46c07576a3684bb1cf1064cca7f316e7b26a59f84219e186c93d02a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Mon, 17 Nov 2025 23:31:23 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GOSU_VERSION=1.19
# Mon, 17 Nov 2025 23:31:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Nov 2025 23:31:25 GMT
ENV NODE_ENV=production
# Mon, 17 Nov 2025 23:31:25 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 17 Nov 2025 23:31:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 17 Nov 2025 23:31:40 GMT
ENV GHOST_VERSION=6.8.1
# Mon, 17 Nov 2025 23:34:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
WORKDIR /var/lib/ghost
# Mon, 17 Nov 2025 23:34:30 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 17 Nov 2025 23:34:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:34:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:34:30 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 17 Nov 2025 23:34:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1827a5c4524186118eee00a4ac63d63193f596b938559b665bc04324b9ad1f`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ee73bf02cc21d58721e5860fb78e417016e95199c7ae7200ae0bda2dbf2c7`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 876.4 KB (876367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d64b7446ae5dc06d711f1426ee8b76d3347a12a6d4cc5e6d7d7ae1761303bf`  
		Last Modified: Mon, 17 Nov 2025 23:35:18 GMT  
		Size: 11.7 MB (11667754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5d1df407927fc4fbb55e170799a247fa44e76425b5ff769e66d933373a4e6`  
		Last Modified: Tue, 18 Nov 2025 01:46:15 GMT  
		Size: 138.3 MB (138275091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4cc7c18b66830086b72324d1b2c0364f34d7957eecf34ca1dc59641b9c2ed`  
		Last Modified: Mon, 17 Nov 2025 23:35:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:4ccf5fb9eaf7257f301bde1e1b23cedc1a75d066833c8d112c1c54bcff537ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade1dc922fe906e118c634045e294e4e4f5291540c9139ecf4e0e840661d059`

```dockerfile
```

-	Layers:
	-	`sha256:95ee7b85f3cdd1151d26ba89ad27a6c99e15d81e1a1c4ee8caf308c16d0384c6`  
		Last Modified: Tue, 18 Nov 2025 01:45:40 GMT  
		Size: 3.4 MB (3397746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074563961effd80c19f806f12fa2242710f6c81daf01ea409984a48be72be4cd`  
		Last Modified: Tue, 18 Nov 2025 01:45:41 GMT  
		Size: 26.6 KB (26572 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:0c70f4153a05e875c046bf2a763ecd1d47ff403ba2b35c3af5a3fcbe76ded772
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
$ docker pull ghost@sha256:fd792d31faf9c72ce1132b43732e3b996afc010bcd67fd7e1769a8a5e21ea83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220015950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e76b55d62ee5f57a2f2629587dae1b49d039b851cfd02aa24a8b884778f14b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:26:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 05:29:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:29:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:29:58 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:00 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:11:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:11:24 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:24 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:11:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942578950a9229a852f0de33e4e5ff14a882d26d1ca25de0d239c09ae1a3271b`  
		Last Modified: Tue, 18 Nov 2025 05:27:35 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e6aad59bf1a2f3111ba30aeba5544b0a5379113ea4cc61f8bbf1acfb442dba`  
		Last Modified: Tue, 18 Nov 2025 05:30:22 GMT  
		Size: 49.5 MB (49481526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f7d23d4cdc8c290c919165cf1a555f4d5197ee7046c0429ae5de36bb3fda3`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419608b38e593ad78de784c2b22c7f3ae8d1ba15dbf8dbe3fabeffa3c27419e`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b056b2197ec736f8cf7d1b5887359b81357b2690f31b41d6a5155ad80f7e6398`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 1.2 MB (1247533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759e78cde27ef7836641c7142a7b88209d66c23975a490fc46732a70f9e7d44`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 11.7 MB (11663639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d2b2ac02b40714cc61f7c2f937f590709ee929c9954446f2ae6b3a12d7914`  
		Last Modified: Tue, 18 Nov 2025 07:12:24 GMT  
		Size: 127.7 MB (127677853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc938c3386ad45611101bef76a38a4bf1f712d9860dd254474e8e7c4b7e4bb6`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:3769437c228cc33bd6f6314944b2e33911dbde5d7f1a3eb4e3b6168af01c4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd9ec508f22d54d19243d894a399e7e34ca0edbca7371a59dee24128afbf136`

```dockerfile
```

-	Layers:
	-	`sha256:26893031743eec8901db1bc6c96b5e1929b55ee0d486add4de745550f403c12d`  
		Last Modified: Tue, 18 Nov 2025 10:46:21 GMT  
		Size: 5.6 MB (5610688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcd49853fa4834880a3f1e656a1f7b1954facb85a8a45fa9db8b1522912b701`  
		Last Modified: Tue, 18 Nov 2025 10:46:22 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:995cd65fa2aca91e83eda3c71ce1a5461bd7a49e7a1935709399ebccd7c561fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a05ab353924aacdfdbef47cf48d7514682ec29306f87753a44d82f116cd4b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:23:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:51 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:32 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:29:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:43 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:43 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0647d91c59ce8c8d984e0d8a464ae67e3d18cfba6e102b4b9df3d23ace254886`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aec5cbb97a45b1295e632f50a486c86084369aba94dcb9baaa4b2f589a919d`  
		Last Modified: Tue, 18 Nov 2025 04:24:13 GMT  
		Size: 44.2 MB (44208140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f8dd114fc0077d2ef22d4e7ad09dfb945a9b18a58e75b6f237ee4f59717128`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 1.7 MB (1712780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f611703056a722d286e4abea947d6f7a29129d37ff2a28dd02acd739d1e7a117`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7a6a6416d331bfe046423b73e51e0d89e36462eb2f3a188c96d27790d3f5c`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb7ce7a5a3dfdbd679fce04e3d38f147d35993f0a57a64124074dd94c987d3`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 11.7 MB (11660200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0061525f729d8f190bd0bdd8299b65cb3f62c7faf5afa8d39ecfc8ec65e41ab`  
		Last Modified: Tue, 18 Nov 2025 11:23:42 GMT  
		Size: 128.7 MB (128736935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d24192eb8d1f6db02dee05b0e3170dc7dade4de7ce93f4884601941bda9c0b`  
		Last Modified: Tue, 18 Nov 2025 07:30:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:756bd77b45dcb6d61c042d770075e103fd51c6586116befc831c5da9b223e907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce12acf64e85084b7377e248875df8d50c73ba6aa09a3d0ffca6bee6b78fe1fb`

```dockerfile
```

-	Layers:
	-	`sha256:0aee169b1ffcc2e456f4bc5da786961494f1a149dc121d484a6c1773de9be757`  
		Last Modified: Tue, 18 Nov 2025 10:46:26 GMT  
		Size: 5.6 MB (5613487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0cff61496ff7e4381947023547bc08fa851c8aa79348e8ea0babc1a599e6fc`  
		Last Modified: Tue, 18 Nov 2025 10:46:27 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:258c4407d6d7bce9f9eef454ae918168b9905ae91fad8e2c6784d3eed4819cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220074205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8399decb593f9e243b712665934c16a889eae908e7e077dc1a77f256824c57bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:03:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:03:44 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:44 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:15:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:15:49 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:17 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 06:18:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:18:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:18:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e88625ec434b2584983383ce17b9544a3c599a885f7dcd0ca01d5804a1eec3a`  
		Last Modified: Tue, 18 Nov 2025 03:58:47 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26974ee5c741410e72a5aaeeee45d4377f5d2c1a52f3a56c09a97bb8abce5f`  
		Last Modified: Tue, 18 Nov 2025 04:04:11 GMT  
		Size: 49.6 MB (49614746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393386629f425518f5340811baae8dc86203636e0049338341c222e66e3057ef`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26540316edc055fdeb9b9eebee982d07ce412a09a722e07f64f64bd398cdfced`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715eee0464cfc96ba6c1b685fb3f359b828a0c7e7d2b8be0222d5d5544c484c7`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 1.2 MB (1201406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8035a91ebbd314903564682e0e427992e79d7a14fb0eafad2c71e4a002f573`  
		Last Modified: Tue, 18 Nov 2025 06:19:33 GMT  
		Size: 11.7 MB (11666371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980312c520ebcbad91e097ac0916660d49c7b05de98f424f6151f0b9917300e7`  
		Last Modified: Tue, 18 Nov 2025 06:19:41 GMT  
		Size: 127.8 MB (127772562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083639d9f6e238da2de3217eba8c3ada171926da1a0866fff6206396526bff59`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:cc9b52228daba5c3e2f262152adb0efa70f07d276b8ffc6db69d60df2a9c169e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7606ad196d35ba7f0d10c58e0ae40aab5321270a3e7435031ba435b0ae49fe`

```dockerfile
```

-	Layers:
	-	`sha256:b848dd81ea7646f37749d26fc92914936bf8af1ef6b71e659ad53df002a56dc2`  
		Last Modified: Tue, 18 Nov 2025 07:46:51 GMT  
		Size: 5.6 MB (5611039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b84ad264e41bccd5cfc9d153f75624e06803a68097e7c909ff538218ae37d9`  
		Last Modified: Tue, 18 Nov 2025 07:46:52 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c3f1e7ead6676aa1584be14ebf9d9b4550b6bc1bbe396ed49bdf5e77de7eace3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3452894f8734c3d058ea4cb0278c7d8fa1cb40be4b6125260abd4f095a18980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:11:39 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:11:55 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:12:04 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:12:04 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:04 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:03:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:45 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:45 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:46 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499a8c640bba2d2c845b32a54d35f79f91741fefd38b97e1da3f71e752be2382`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31a3dad6a431bde6ec5161ea2c1432c62d82552cf9303600f3e2746dcd4ee`  
		Last Modified: Tue, 18 Nov 2025 04:12:41 GMT  
		Size: 49.7 MB (49676885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b22afc160ee4d6820ca8130d8a93d583df65df36055faf0e8e553aaf57bb6ff`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf53011c4bc2010e35980a5a682d5882000d36c5b385c845afd82173abd258e`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f8ef58685220dfe83dd97c2b3dcea755e6c7049e6231fd97aa8a3133c94a72`  
		Last Modified: Tue, 18 Nov 2025 07:05:39 GMT  
		Size: 1.2 MB (1221443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cb90fd75a53807b356490ca5520a75993c61c5f320395a463fb2f245bdf055`  
		Last Modified: Tue, 18 Nov 2025 07:05:40 GMT  
		Size: 11.7 MB (11682323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fea2233ae68d7080525c5311d18fc2f141032987f0a6e4cecc6bf5ebbaa4b0`  
		Last Modified: Tue, 18 Nov 2025 10:08:27 GMT  
		Size: 130.8 MB (130810057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26afe088044265f6245c4c21b84d4fdf063cb1b784fb14a98eaa4cedce49aac`  
		Last Modified: Tue, 18 Nov 2025 07:05:38 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:e5e321b7cf2edae165e31379ee8b70220005b0a967950527a781ed57d459276a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4febf40b76ebf8f90523a5585f55fe64a8fcad6666bb8c4401d39082d745de1a`

```dockerfile
```

-	Layers:
	-	`sha256:63284f20b241d705bc393f6fa2f4a5fa5835d07e057507c4aacc98450713b979`  
		Last Modified: Tue, 18 Nov 2025 07:46:57 GMT  
		Size: 5.6 MB (5604515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c087b81d1871251fef1c8126ce47429ffbd371565c5030a4595d4af5df7ad4be`  
		Last Modified: Tue, 18 Nov 2025 07:46:58 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:0c70f4153a05e875c046bf2a763ecd1d47ff403ba2b35c3af5a3fcbe76ded772
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
$ docker pull ghost@sha256:fd792d31faf9c72ce1132b43732e3b996afc010bcd67fd7e1769a8a5e21ea83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220015950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e76b55d62ee5f57a2f2629587dae1b49d039b851cfd02aa24a8b884778f14b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:26:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 05:29:45 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:45 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 05:29:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:29:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:29:58 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:09:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:09:00 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:09:00 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:09:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:09:20 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:11:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:11:24 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:24 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:11:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942578950a9229a852f0de33e4e5ff14a882d26d1ca25de0d239c09ae1a3271b`  
		Last Modified: Tue, 18 Nov 2025 05:27:35 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e6aad59bf1a2f3111ba30aeba5544b0a5379113ea4cc61f8bbf1acfb442dba`  
		Last Modified: Tue, 18 Nov 2025 05:30:22 GMT  
		Size: 49.5 MB (49481526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f7d23d4cdc8c290c919165cf1a555f4d5197ee7046c0429ae5de36bb3fda3`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 1.7 MB (1712618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419608b38e593ad78de784c2b22c7f3ae8d1ba15dbf8dbe3fabeffa3c27419e`  
		Last Modified: Tue, 18 Nov 2025 05:30:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b056b2197ec736f8cf7d1b5887359b81357b2690f31b41d6a5155ad80f7e6398`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 1.2 MB (1247533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759e78cde27ef7836641c7142a7b88209d66c23975a490fc46732a70f9e7d44`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 11.7 MB (11663639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d2b2ac02b40714cc61f7c2f937f590709ee929c9954446f2ae6b3a12d7914`  
		Last Modified: Tue, 18 Nov 2025 07:12:24 GMT  
		Size: 127.7 MB (127677853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc938c3386ad45611101bef76a38a4bf1f712d9860dd254474e8e7c4b7e4bb6`  
		Last Modified: Tue, 18 Nov 2025 07:12:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:3769437c228cc33bd6f6314944b2e33911dbde5d7f1a3eb4e3b6168af01c4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd9ec508f22d54d19243d894a399e7e34ca0edbca7371a59dee24128afbf136`

```dockerfile
```

-	Layers:
	-	`sha256:26893031743eec8901db1bc6c96b5e1929b55ee0d486add4de745550f403c12d`  
		Last Modified: Tue, 18 Nov 2025 10:46:21 GMT  
		Size: 5.6 MB (5610688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcd49853fa4834880a3f1e656a1f7b1954facb85a8a45fa9db8b1522912b701`  
		Last Modified: Tue, 18 Nov 2025 10:46:22 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:995cd65fa2aca91e83eda3c71ce1a5461bd7a49e7a1935709399ebccd7c561fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a05ab353924aacdfdbef47cf48d7514682ec29306f87753a44d82f116cd4b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:23:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:38 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:23:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:23:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:23:51 GMT
CMD ["node"]
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 07:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 07:26:32 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 07:26:32 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 07:26:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 07:26:49 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:29:42 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:29:43 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:43 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:29:43 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0647d91c59ce8c8d984e0d8a464ae67e3d18cfba6e102b4b9df3d23ace254886`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aec5cbb97a45b1295e632f50a486c86084369aba94dcb9baaa4b2f589a919d`  
		Last Modified: Tue, 18 Nov 2025 04:24:13 GMT  
		Size: 44.2 MB (44208140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f8dd114fc0077d2ef22d4e7ad09dfb945a9b18a58e75b6f237ee4f59717128`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 1.7 MB (1712780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f611703056a722d286e4abea947d6f7a29129d37ff2a28dd02acd739d1e7a117`  
		Last Modified: Tue, 18 Nov 2025 04:24:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7a6a6416d331bfe046423b73e51e0d89e36462eb2f3a188c96d27790d3f5c`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 1.2 MB (1214315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb7ce7a5a3dfdbd679fce04e3d38f147d35993f0a57a64124074dd94c987d3`  
		Last Modified: Tue, 18 Nov 2025 07:30:29 GMT  
		Size: 11.7 MB (11660200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0061525f729d8f190bd0bdd8299b65cb3f62c7faf5afa8d39ecfc8ec65e41ab`  
		Last Modified: Tue, 18 Nov 2025 11:23:42 GMT  
		Size: 128.7 MB (128736935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d24192eb8d1f6db02dee05b0e3170dc7dade4de7ce93f4884601941bda9c0b`  
		Last Modified: Tue, 18 Nov 2025 07:30:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:756bd77b45dcb6d61c042d770075e103fd51c6586116befc831c5da9b223e907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce12acf64e85084b7377e248875df8d50c73ba6aa09a3d0ffca6bee6b78fe1fb`

```dockerfile
```

-	Layers:
	-	`sha256:0aee169b1ffcc2e456f4bc5da786961494f1a149dc121d484a6c1773de9be757`  
		Last Modified: Tue, 18 Nov 2025 10:46:26 GMT  
		Size: 5.6 MB (5613487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0cff61496ff7e4381947023547bc08fa851c8aa79348e8ea0babc1a599e6fc`  
		Last Modified: Tue, 18 Nov 2025 10:46:27 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:258c4407d6d7bce9f9eef454ae918168b9905ae91fad8e2c6784d3eed4819cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220074205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8399decb593f9e243b712665934c16a889eae908e7e077dc1a77f256824c57bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:03:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:03:44 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:44 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:15:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:15:49 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:15:49 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:16:17 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:16:17 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 06:18:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 06:18:44 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 06:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:44 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 06:18:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e88625ec434b2584983383ce17b9544a3c599a885f7dcd0ca01d5804a1eec3a`  
		Last Modified: Tue, 18 Nov 2025 03:58:47 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26974ee5c741410e72a5aaeeee45d4377f5d2c1a52f3a56c09a97bb8abce5f`  
		Last Modified: Tue, 18 Nov 2025 04:04:11 GMT  
		Size: 49.6 MB (49614746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393386629f425518f5340811baae8dc86203636e0049338341c222e66e3057ef`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26540316edc055fdeb9b9eebee982d07ce412a09a722e07f64f64bd398cdfced`  
		Last Modified: Tue, 18 Nov 2025 04:04:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715eee0464cfc96ba6c1b685fb3f359b828a0c7e7d2b8be0222d5d5544c484c7`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 1.2 MB (1201406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8035a91ebbd314903564682e0e427992e79d7a14fb0eafad2c71e4a002f573`  
		Last Modified: Tue, 18 Nov 2025 06:19:33 GMT  
		Size: 11.7 MB (11666371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980312c520ebcbad91e097ac0916660d49c7b05de98f424f6151f0b9917300e7`  
		Last Modified: Tue, 18 Nov 2025 06:19:41 GMT  
		Size: 127.8 MB (127772562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083639d9f6e238da2de3217eba8c3ada171926da1a0866fff6206396526bff59`  
		Last Modified: Tue, 18 Nov 2025 06:19:32 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:cc9b52228daba5c3e2f262152adb0efa70f07d276b8ffc6db69d60df2a9c169e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7606ad196d35ba7f0d10c58e0ae40aab5321270a3e7435031ba435b0ae49fe`

```dockerfile
```

-	Layers:
	-	`sha256:b848dd81ea7646f37749d26fc92914936bf8af1ef6b71e659ad53df002a56dc2`  
		Last Modified: Tue, 18 Nov 2025 07:46:51 GMT  
		Size: 5.6 MB (5611039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b84ad264e41bccd5cfc9d153f75624e06803a68097e7c909ff538218ae37d9`  
		Last Modified: Tue, 18 Nov 2025 07:46:52 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:c3f1e7ead6676aa1584be14ebf9d9b4550b6bc1bbe396ed49bdf5e77de7eace3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3452894f8734c3d058ea4cb0278c7d8fa1cb40be4b6125260abd4f095a18980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:11:39 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV NODE_VERSION=22.21.1
# Tue, 18 Nov 2025 04:11:55 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:11:55 GMT
ENV YARN_VERSION=1.22.22
# Tue, 18 Nov 2025 04:12:04 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:12:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:12:04 GMT
CMD ["node"]
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 06:56:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 06:56:04 GMT
ENV NODE_ENV=production
# Tue, 18 Nov 2025 06:56:04 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 18 Nov 2025 06:56:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 18 Nov 2025 06:56:38 GMT
ENV GHOST_VERSION=6.8.1
# Tue, 18 Nov 2025 07:03:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 18 Nov 2025 07:03:45 GMT
WORKDIR /var/lib/ghost
# Tue, 18 Nov 2025 07:03:45 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 18 Nov 2025 07:03:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:46 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 18 Nov 2025 07:03:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499a8c640bba2d2c845b32a54d35f79f91741fefd38b97e1da3f71e752be2382`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31a3dad6a431bde6ec5161ea2c1432c62d82552cf9303600f3e2746dcd4ee`  
		Last Modified: Tue, 18 Nov 2025 04:12:41 GMT  
		Size: 49.7 MB (49676885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b22afc160ee4d6820ca8130d8a93d583df65df36055faf0e8e553aaf57bb6ff`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf53011c4bc2010e35980a5a682d5882000d36c5b385c845afd82173abd258e`  
		Last Modified: Tue, 18 Nov 2025 04:12:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f8ef58685220dfe83dd97c2b3dcea755e6c7049e6231fd97aa8a3133c94a72`  
		Last Modified: Tue, 18 Nov 2025 07:05:39 GMT  
		Size: 1.2 MB (1221443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cb90fd75a53807b356490ca5520a75993c61c5f320395a463fb2f245bdf055`  
		Last Modified: Tue, 18 Nov 2025 07:05:40 GMT  
		Size: 11.7 MB (11682323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fea2233ae68d7080525c5311d18fc2f141032987f0a6e4cecc6bf5ebbaa4b0`  
		Last Modified: Tue, 18 Nov 2025 10:08:27 GMT  
		Size: 130.8 MB (130810057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26afe088044265f6245c4c21b84d4fdf063cb1b784fb14a98eaa4cedce49aac`  
		Last Modified: Tue, 18 Nov 2025 07:05:38 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:e5e321b7cf2edae165e31379ee8b70220005b0a967950527a781ed57d459276a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4febf40b76ebf8f90523a5585f55fe64a8fcad6666bb8c4401d39082d745de1a`

```dockerfile
```

-	Layers:
	-	`sha256:63284f20b241d705bc393f6fa2f4a5fa5835d07e057507c4aacc98450713b979`  
		Last Modified: Tue, 18 Nov 2025 07:46:57 GMT  
		Size: 5.6 MB (5604515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c087b81d1871251fef1c8126ce47429ffbd371565c5030a4595d4af5df7ad4be`  
		Last Modified: Tue, 18 Nov 2025 07:46:58 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

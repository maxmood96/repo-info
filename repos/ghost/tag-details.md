<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5-alpine3.23`](#ghost5-alpine323)
-	[`ghost:5-bookworm`](#ghost5-bookworm)
-	[`ghost:5.130`](#ghost5130)
-	[`ghost:5.130-alpine`](#ghost5130-alpine)
-	[`ghost:5.130-alpine3.23`](#ghost5130-alpine323)
-	[`ghost:5.130-bookworm`](#ghost5130-bookworm)
-	[`ghost:5.130.6`](#ghost51306)
-	[`ghost:5.130.6-alpine`](#ghost51306-alpine)
-	[`ghost:5.130.6-alpine3.23`](#ghost51306-alpine323)
-	[`ghost:5.130.6-bookworm`](#ghost51306-bookworm)
-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.23`](#ghost6-alpine323)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.17`](#ghost617)
-	[`ghost:6.17-alpine`](#ghost617-alpine)
-	[`ghost:6.17-alpine3.23`](#ghost617-alpine323)
-	[`ghost:6.17-bookworm`](#ghost617-bookworm)
-	[`ghost:6.17.0`](#ghost6170)
-	[`ghost:6.17.0-alpine`](#ghost6170-alpine)
-	[`ghost:6.17.0-alpine3.23`](#ghost6170-alpine323)
-	[`ghost:6.17.0-bookworm`](#ghost6170-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.23`](#ghostalpine323)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:3ffcb8f2f1f808806e7a0f694a2b130cd78652a26b4337b33fe7e249ce58665a
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
$ docker pull ghost@sha256:db4c990b507f9063e9e1428ea59867bf39f5ebad42246eb1b17cf00ed8b4ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201754407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71366308fc2caced336681cfa4957cee899317205f37f9c325c0e8dbda1204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:49:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:50:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:44:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:44:11 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 03:44:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 03:45:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 03:45:32 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 03:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 03:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:33 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 03:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66d95167c29e1f4d0399617e49250519defda4aa8ea5919064ab3dbd6f0627`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0393491048e0b5148349736f25b7d015e244fee9ab757ef2b0824dc65f3bb9`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 41.0 MB (40982963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a2dcd5a595e7a3d71eacdb266b1f3057397d8a882e9d5a7e55214ea80a21f`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa087727009d9926282b77e9386998f27b6535e550659c7fc1d4ea3b9a973bd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b419252a0ee203e9bebcd21b87684a2d76438133357d02fe0397715d741fc4`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 1.2 MB (1247602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8b2596b3af8b6296ede9aaf62a9409757108296aa7e91263ec687da5b947f`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 11.6 MB (11554942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad0c0054ec5e4c7b33e2ca938892a3c7c44d785c6b34b4724015c6f8ca5a4`  
		Last Modified: Tue, 03 Feb 2026 03:46:08 GMT  
		Size: 118.0 MB (118023390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecf05c1e84beea5440a8eddc45bc88faf593b42c4021c19b754b870beba47e`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:af1ca98cafd5169ff18998e596fbedcbfec146d9d1f115d1c7ad4f1523e8b512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbfd6c3ff5df35ad558360576ba86f301ae29dbeb1661875b0b512a04dbd002`

```dockerfile
```

-	Layers:
	-	`sha256:9a12d1103a71abb258b1ae91ca81660f943d79371130705776728d5f06314db6`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 5.6 MB (5638448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5c4708c40af9d4081f66718d7a3a3303f1792edf265c44dad507ba7307e406`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:412a891307603ff60265ff535ca07935cd21449bc3a84f19de4a8d39fb5efe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1a7b0d9b80b754520077c154cc7c122ba490be5c544a64af1f93b87bca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:44:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:44:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:44:23 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:16:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:16:34 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:16:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 05:19:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 05:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:36 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f422e3c8e3483b692ceb6f1d2306cabd7f3e6ecc011ba439e95fce34211d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389e52b4174b3a27b61d3f3aa39018a05e20e68d45fbc464a033a4cc380b19b`  
		Last Modified: Tue, 03 Feb 2026 03:44:36 GMT  
		Size: 37.1 MB (37069744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150d5e1afc02a2e46573c8916f0eef87261b4a20cfcad96622ce25ee34cce0d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c55cc18845c75a0db840e1e7b90ad6aa20cc9a8a465124e98aaca205349c9`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e19cf73ee54c7198a0b4f1cbc75b012a1de3938816e18861de3e9d7064f1a`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 1.2 MB (1214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1584472094f5e70f3cca202c7d7a9a521468469284b06f6952ea8eebb0cc68`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 11.6 MB (11555370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23718c2c85accf68e18880a9fc2553f339ba5bef470759c3eaf601b076ecc60`  
		Last Modified: Tue, 03 Feb 2026 05:20:24 GMT  
		Size: 120.6 MB (120584972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3816c666a0e46bf06d39ff06f7c2085f26641e044563411b9b6b7261a95e9`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:835575588bd50edfbe344e957b632dc775be34fed1b5d23f5d18b6888b2a9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d9ad5efa0023f7877c8f800f52b4d53502da8b14e2a5b4c70f86dc25102bd3`

```dockerfile
```

-	Layers:
	-	`sha256:448479178972e381d44e8ec311fc1dbad068faff364e6abaf16660fbb0052be4`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 5.6 MB (5641227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7f4f119d555f4e4c13abdc6b7f5b3a5527d141dd2eac8c5b34588cf942105c`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2f84ae2826bd5b8c1d62628a9ae141b8daec3ed8196d59ffb35346caa05798d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201644231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6aeb7812b275d2d5c26e0a1e4a15acae571e7e40b279d147254d0974e0a81e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:52:33 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:45 GMT
CMD ["node"]
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 04:02:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:02:33 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 04:02:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 04:03:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 04:03:57 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 04:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 04:03:57 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 04:03:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a57bb448d9d8de948e9dfd590e065bb48b5625f7f3b2357c3d66b0da9385`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5334ad83891f85d8537efda275fb71a38a0ada55de771b01c808696232729e0`  
		Last Modified: Tue, 03 Feb 2026 02:53:00 GMT  
		Size: 40.9 MB (40939901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731fb92622470b249c590dc9989be6eaa305251fcb1a5b10ca39d4dcc1c865e`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 1.7 MB (1712602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ce91b8c1d5319a42f2216f1f01ef2aa9546df8ff67be5359146ef34bed80d`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8ef36ef2eb0f9eed5827f821270c37843c518a42bc56b3a79f1029634934c`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 1.2 MB (1201482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf275a028303067f8f30d7cc4598944fcf23ba7d09fddac9f2fdebe5b60c933`  
		Last Modified: Tue, 03 Feb 2026 04:04:32 GMT  
		Size: 11.6 MB (11555247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049cccc3badf5abca466e8eac954fe22a63b2bb1059b35bdf3d9ab817010b443`  
		Last Modified: Tue, 03 Feb 2026 04:04:34 GMT  
		Size: 118.1 MB (118122845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b57f2b897d4abdacaae87cf7f2ae379e429eab83a84b7ee7317e2464a149c9`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:a1dd5d32fd09cd6c374c9a0537eddb7362a8ac0d359531c1f1fc385f8f54b74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608cb4c6896bdc5c6c8b5c8f70af50f44802a29ad5166812884fad2c0903a05`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbeea38fc4479a758bc51cc76900eee05586652212af68be415386c9857c43`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 5.6 MB (5638775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26afdb16f65877a6886579fc0b3cd0e829c498231c0b55d41376ee58fdd26f1b`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:c8144f93af0dd291877d9de1c84a2fa04cc34bb0f9b106ae8d2bdd03e050d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205275425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2fb5c654eaa45e3f6baea2602d5b37d7da9f8bc36c8cef0faf46db2bbdc0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:49:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:51:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:52:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:52:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:59:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:59:31 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:59:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 06:02:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 06:02:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 06:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 06:02:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 06:02:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466ebe0ea905076601b8793254dc31d06b3c76b4d8c4bc3b3053cea0110fb4`  
		Last Modified: Tue, 03 Feb 2026 03:50:01 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5fee3e4eaedf9ac67494a71ce92d031c95788c11ee7afbcdaf7611ca00c50`  
		Last Modified: Tue, 03 Feb 2026 03:52:24 GMT  
		Size: 41.2 MB (41234983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee9d0b0428acaedd477f0aa13962b11044dccc937b415940e62ddc3eb61910`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 1.7 MB (1712656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761b4060e7745b76cc6769879475967fb0a6111ca136ed952547976e3982017`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f344302285e0a2d20bb95d612920aae7161c801d09c78a90390d5f8c3a973`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 1.2 MB (1221387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fdcc29d6fa001a8fd40b696cd24ca5743a566a8386eabe882234198ff7a17`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 11.6 MB (11555055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce51c47940052e76b56be3d3b5a54ffba7b2918aab72497a00815408065dd`  
		Last Modified: Tue, 03 Feb 2026 06:02:59 GMT  
		Size: 122.7 MB (122662629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61796f50ec62726694a165792a31ce33d49685d04549abf60827f033df5ccf43`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:f4cfd435be2033a741f33edd4c00fb15b3dea8eb934f880316a2d2dbdbcf2589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3aa99b883df392ee8f8918ebba26b085b5d5258c34d8ab7e89526833fe05c`

```dockerfile
```

-	Layers:
	-	`sha256:aab5d6c9625cefc1fc47c3d31a33ed461bc9e942342f83d5780c3fff98e9074e`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 5.6 MB (5632271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4326dc0654079c60e784576195910e3b78068d72326a0b530a0e87693c589158`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:a0506f3f05f5bdc6c950c5113cdcdb1e1f96fbf15f6dc0a39fc093c25348bdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:2341e27e1f3f8496f677f77d0620c1d514e2f4111708bbc03e8bc7c9d39a36fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176143724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e42e1a27813280c68141d3b31ee65c5c729991780f12368265d3615a49db2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:46 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:31:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:49 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:48:42 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:49:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:49:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:49:53 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:49:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:49:54 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:49:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d96c196e3198e14ea37df8bba4f54bf92fb525eb65e49fa4027c7dee13f80`  
		Last Modified: Wed, 28 Jan 2026 03:32:03 GMT  
		Size: 42.8 MB (42782769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87f4721c91769ed5206f34a9ab6ec98fc1d5235c12c2fc956665b1155e9ecb`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 1.3 MB (1262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31b2016552274339ed88ed4a438d78bf37e0f6bdf328d02207b2a598c1ef86d`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a106b9634effefe3ddbf2725d5e37a5fb2edb5e62e7d4a88e76158a4e2abf08`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 821.9 KB (821902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a0aaa90ef05be2fd9a6b377ddd409cbc2f1e843317c63a56495971394db3`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 928.3 KB (928325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97ac866edba5d8600572c2a8389a73fc66e6a385fd4cdf361943c6dfd5d5153`  
		Last Modified: Sun, 01 Feb 2026 07:50:25 GMT  
		Size: 11.6 MB (11579070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32fa910c76f8d8d715c5009b6fa028af53efa371e036e4d44937d8f9ac183a`  
		Last Modified: Sun, 01 Feb 2026 07:50:27 GMT  
		Size: 114.9 MB (114906695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d67e8a832c42b678355b580b89c275badc50789b2ea15430a0b88b1d99a2c`  
		Last Modified: Sun, 01 Feb 2026 07:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06a707175e55a16a6c1c2e4d6a38e86a58afcf312e2f091bfd90f971d304d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56188cd2919f3be565558fb22e57d214985876a4ce7b6957051f08cafcc37e99`

```dockerfile
```

-	Layers:
	-	`sha256:708bd681f03f1f02a74465d20e6d7dec4f9c997af10cbd320f990166a658ad88`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 3.4 MB (3425676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b3739c1900fa76d1e054ec85a8f05443844de716a5f43a652d5b459b045011`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:acd876f9ac707349b5f43fb3a3ec675f904d6d49d2e8db812b6a90c9c163ae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578900d1d08bdebdb3e3097c0141be06de6a868b626ff3817b707002ff826f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:38:48 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:38:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:48 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:38:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:38:51 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:53:35 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:53:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:55:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:55:12 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:55:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:55:12 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:55:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb920e5d251bfb3a5bac54cb1ee6be01e588068fecdf867141fb05734cd3df8`  
		Last Modified: Wed, 28 Jan 2026 03:39:05 GMT  
		Size: 43.1 MB (43121286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e17969cb2d3834a243108c5903feec6ca60dc3607b03867527e15914e86f6a`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d38c2ed5610a9544ddba1a8feb24733822e5c9409816c26c858d2a270efa7`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112be90c7b1dd2681312ed79d221f223ed46b135256091c4d3a99915ef5744b4`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 891.3 KB (891312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a903efa9ccd32343996cb58aaae2cb6e32f11173d18b3926546670ebaae6b9`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 881.3 KB (881297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92085bba5cf6d1a5c82fb89e5588a678313f3885f83cae6b791c9a8d6c7dc40`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 11.6 MB (11580799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb5a1af78d27870aa99a61809a908a85c8dc5d8164ec80e3e2550498714e0f`  
		Last Modified: Sun, 01 Feb 2026 07:55:49 GMT  
		Size: 125.4 MB (125419264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a916ea2e7c6d7950663e4539112347c987bb9902473c56df80589b4ca77f52`  
		Last Modified: Sun, 01 Feb 2026 07:55:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:704554090da3b5a05719f458094167d96eab2a7641e06c81f9bba913cf4f27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5bd03afee28985b232ade1d38440e59782e2fd2bc56cb125fa688d6fbe69b`

```dockerfile
```

-	Layers:
	-	`sha256:72074f0637949691651a4ba1a2fcb6bde15344ef2aa0a06ec73071d862f3b6a0`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 3.4 MB (3425158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8237d498768cfe460a2674de812a5ce8956474f52e7ee6e364d84c68b94d14fa`  
		Last Modified: Sun, 01 Feb 2026 07:55:46 GMT  
		Size: 26.0 KB (25967 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine3.23`

```console
$ docker pull ghost@sha256:a0506f3f05f5bdc6c950c5113cdcdb1e1f96fbf15f6dc0a39fc093c25348bdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:2341e27e1f3f8496f677f77d0620c1d514e2f4111708bbc03e8bc7c9d39a36fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176143724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e42e1a27813280c68141d3b31ee65c5c729991780f12368265d3615a49db2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:46 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:31:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:49 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:48:42 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:49:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:49:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:49:53 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:49:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:49:54 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:49:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d96c196e3198e14ea37df8bba4f54bf92fb525eb65e49fa4027c7dee13f80`  
		Last Modified: Wed, 28 Jan 2026 03:32:03 GMT  
		Size: 42.8 MB (42782769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87f4721c91769ed5206f34a9ab6ec98fc1d5235c12c2fc956665b1155e9ecb`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 1.3 MB (1262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31b2016552274339ed88ed4a438d78bf37e0f6bdf328d02207b2a598c1ef86d`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a106b9634effefe3ddbf2725d5e37a5fb2edb5e62e7d4a88e76158a4e2abf08`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 821.9 KB (821902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a0aaa90ef05be2fd9a6b377ddd409cbc2f1e843317c63a56495971394db3`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 928.3 KB (928325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97ac866edba5d8600572c2a8389a73fc66e6a385fd4cdf361943c6dfd5d5153`  
		Last Modified: Sun, 01 Feb 2026 07:50:25 GMT  
		Size: 11.6 MB (11579070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32fa910c76f8d8d715c5009b6fa028af53efa371e036e4d44937d8f9ac183a`  
		Last Modified: Sun, 01 Feb 2026 07:50:27 GMT  
		Size: 114.9 MB (114906695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d67e8a832c42b678355b580b89c275badc50789b2ea15430a0b88b1d99a2c`  
		Last Modified: Sun, 01 Feb 2026 07:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:06a707175e55a16a6c1c2e4d6a38e86a58afcf312e2f091bfd90f971d304d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56188cd2919f3be565558fb22e57d214985876a4ce7b6957051f08cafcc37e99`

```dockerfile
```

-	Layers:
	-	`sha256:708bd681f03f1f02a74465d20e6d7dec4f9c997af10cbd320f990166a658ad88`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 3.4 MB (3425676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b3739c1900fa76d1e054ec85a8f05443844de716a5f43a652d5b459b045011`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:acd876f9ac707349b5f43fb3a3ec675f904d6d49d2e8db812b6a90c9c163ae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578900d1d08bdebdb3e3097c0141be06de6a868b626ff3817b707002ff826f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:38:48 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:38:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:48 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:38:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:38:51 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:53:35 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:53:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:55:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:55:12 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:55:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:55:12 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:55:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb920e5d251bfb3a5bac54cb1ee6be01e588068fecdf867141fb05734cd3df8`  
		Last Modified: Wed, 28 Jan 2026 03:39:05 GMT  
		Size: 43.1 MB (43121286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e17969cb2d3834a243108c5903feec6ca60dc3607b03867527e15914e86f6a`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d38c2ed5610a9544ddba1a8feb24733822e5c9409816c26c858d2a270efa7`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112be90c7b1dd2681312ed79d221f223ed46b135256091c4d3a99915ef5744b4`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 891.3 KB (891312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a903efa9ccd32343996cb58aaae2cb6e32f11173d18b3926546670ebaae6b9`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 881.3 KB (881297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92085bba5cf6d1a5c82fb89e5588a678313f3885f83cae6b791c9a8d6c7dc40`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 11.6 MB (11580799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb5a1af78d27870aa99a61809a908a85c8dc5d8164ec80e3e2550498714e0f`  
		Last Modified: Sun, 01 Feb 2026 07:55:49 GMT  
		Size: 125.4 MB (125419264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a916ea2e7c6d7950663e4539112347c987bb9902473c56df80589b4ca77f52`  
		Last Modified: Sun, 01 Feb 2026 07:55:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:704554090da3b5a05719f458094167d96eab2a7641e06c81f9bba913cf4f27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5bd03afee28985b232ade1d38440e59782e2fd2bc56cb125fa688d6fbe69b`

```dockerfile
```

-	Layers:
	-	`sha256:72074f0637949691651a4ba1a2fcb6bde15344ef2aa0a06ec73071d862f3b6a0`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 3.4 MB (3425158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8237d498768cfe460a2674de812a5ce8956474f52e7ee6e364d84c68b94d14fa`  
		Last Modified: Sun, 01 Feb 2026 07:55:46 GMT  
		Size: 26.0 KB (25967 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-bookworm`

```console
$ docker pull ghost@sha256:3ffcb8f2f1f808806e7a0f694a2b130cd78652a26b4337b33fe7e249ce58665a
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
$ docker pull ghost@sha256:db4c990b507f9063e9e1428ea59867bf39f5ebad42246eb1b17cf00ed8b4ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201754407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71366308fc2caced336681cfa4957cee899317205f37f9c325c0e8dbda1204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:49:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:50:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:44:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:44:11 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 03:44:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 03:45:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 03:45:32 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 03:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 03:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:33 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 03:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66d95167c29e1f4d0399617e49250519defda4aa8ea5919064ab3dbd6f0627`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0393491048e0b5148349736f25b7d015e244fee9ab757ef2b0824dc65f3bb9`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 41.0 MB (40982963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a2dcd5a595e7a3d71eacdb266b1f3057397d8a882e9d5a7e55214ea80a21f`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa087727009d9926282b77e9386998f27b6535e550659c7fc1d4ea3b9a973bd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b419252a0ee203e9bebcd21b87684a2d76438133357d02fe0397715d741fc4`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 1.2 MB (1247602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8b2596b3af8b6296ede9aaf62a9409757108296aa7e91263ec687da5b947f`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 11.6 MB (11554942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad0c0054ec5e4c7b33e2ca938892a3c7c44d785c6b34b4724015c6f8ca5a4`  
		Last Modified: Tue, 03 Feb 2026 03:46:08 GMT  
		Size: 118.0 MB (118023390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecf05c1e84beea5440a8eddc45bc88faf593b42c4021c19b754b870beba47e`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:af1ca98cafd5169ff18998e596fbedcbfec146d9d1f115d1c7ad4f1523e8b512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbfd6c3ff5df35ad558360576ba86f301ae29dbeb1661875b0b512a04dbd002`

```dockerfile
```

-	Layers:
	-	`sha256:9a12d1103a71abb258b1ae91ca81660f943d79371130705776728d5f06314db6`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 5.6 MB (5638448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5c4708c40af9d4081f66718d7a3a3303f1792edf265c44dad507ba7307e406`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:412a891307603ff60265ff535ca07935cd21449bc3a84f19de4a8d39fb5efe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1a7b0d9b80b754520077c154cc7c122ba490be5c544a64af1f93b87bca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:44:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:44:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:44:23 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:16:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:16:34 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:16:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 05:19:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 05:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:36 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f422e3c8e3483b692ceb6f1d2306cabd7f3e6ecc011ba439e95fce34211d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389e52b4174b3a27b61d3f3aa39018a05e20e68d45fbc464a033a4cc380b19b`  
		Last Modified: Tue, 03 Feb 2026 03:44:36 GMT  
		Size: 37.1 MB (37069744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150d5e1afc02a2e46573c8916f0eef87261b4a20cfcad96622ce25ee34cce0d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c55cc18845c75a0db840e1e7b90ad6aa20cc9a8a465124e98aaca205349c9`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e19cf73ee54c7198a0b4f1cbc75b012a1de3938816e18861de3e9d7064f1a`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 1.2 MB (1214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1584472094f5e70f3cca202c7d7a9a521468469284b06f6952ea8eebb0cc68`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 11.6 MB (11555370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23718c2c85accf68e18880a9fc2553f339ba5bef470759c3eaf601b076ecc60`  
		Last Modified: Tue, 03 Feb 2026 05:20:24 GMT  
		Size: 120.6 MB (120584972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3816c666a0e46bf06d39ff06f7c2085f26641e044563411b9b6b7261a95e9`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:835575588bd50edfbe344e957b632dc775be34fed1b5d23f5d18b6888b2a9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d9ad5efa0023f7877c8f800f52b4d53502da8b14e2a5b4c70f86dc25102bd3`

```dockerfile
```

-	Layers:
	-	`sha256:448479178972e381d44e8ec311fc1dbad068faff364e6abaf16660fbb0052be4`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 5.6 MB (5641227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7f4f119d555f4e4c13abdc6b7f5b3a5527d141dd2eac8c5b34588cf942105c`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2f84ae2826bd5b8c1d62628a9ae141b8daec3ed8196d59ffb35346caa05798d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201644231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6aeb7812b275d2d5c26e0a1e4a15acae571e7e40b279d147254d0974e0a81e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:52:33 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:45 GMT
CMD ["node"]
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 04:02:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:02:33 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 04:02:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 04:03:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 04:03:57 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 04:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 04:03:57 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 04:03:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a57bb448d9d8de948e9dfd590e065bb48b5625f7f3b2357c3d66b0da9385`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5334ad83891f85d8537efda275fb71a38a0ada55de771b01c808696232729e0`  
		Last Modified: Tue, 03 Feb 2026 02:53:00 GMT  
		Size: 40.9 MB (40939901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731fb92622470b249c590dc9989be6eaa305251fcb1a5b10ca39d4dcc1c865e`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 1.7 MB (1712602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ce91b8c1d5319a42f2216f1f01ef2aa9546df8ff67be5359146ef34bed80d`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8ef36ef2eb0f9eed5827f821270c37843c518a42bc56b3a79f1029634934c`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 1.2 MB (1201482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf275a028303067f8f30d7cc4598944fcf23ba7d09fddac9f2fdebe5b60c933`  
		Last Modified: Tue, 03 Feb 2026 04:04:32 GMT  
		Size: 11.6 MB (11555247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049cccc3badf5abca466e8eac954fe22a63b2bb1059b35bdf3d9ab817010b443`  
		Last Modified: Tue, 03 Feb 2026 04:04:34 GMT  
		Size: 118.1 MB (118122845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b57f2b897d4abdacaae87cf7f2ae379e429eab83a84b7ee7317e2464a149c9`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a1dd5d32fd09cd6c374c9a0537eddb7362a8ac0d359531c1f1fc385f8f54b74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608cb4c6896bdc5c6c8b5c8f70af50f44802a29ad5166812884fad2c0903a05`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbeea38fc4479a758bc51cc76900eee05586652212af68be415386c9857c43`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 5.6 MB (5638775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26afdb16f65877a6886579fc0b3cd0e829c498231c0b55d41376ee58fdd26f1b`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c8144f93af0dd291877d9de1c84a2fa04cc34bb0f9b106ae8d2bdd03e050d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205275425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2fb5c654eaa45e3f6baea2602d5b37d7da9f8bc36c8cef0faf46db2bbdc0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:49:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:51:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:52:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:52:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:59:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:59:31 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:59:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 06:02:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 06:02:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 06:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 06:02:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 06:02:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466ebe0ea905076601b8793254dc31d06b3c76b4d8c4bc3b3053cea0110fb4`  
		Last Modified: Tue, 03 Feb 2026 03:50:01 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5fee3e4eaedf9ac67494a71ce92d031c95788c11ee7afbcdaf7611ca00c50`  
		Last Modified: Tue, 03 Feb 2026 03:52:24 GMT  
		Size: 41.2 MB (41234983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee9d0b0428acaedd477f0aa13962b11044dccc937b415940e62ddc3eb61910`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 1.7 MB (1712656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761b4060e7745b76cc6769879475967fb0a6111ca136ed952547976e3982017`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f344302285e0a2d20bb95d612920aae7161c801d09c78a90390d5f8c3a973`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 1.2 MB (1221387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fdcc29d6fa001a8fd40b696cd24ca5743a566a8386eabe882234198ff7a17`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 11.6 MB (11555055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce51c47940052e76b56be3d3b5a54ffba7b2918aab72497a00815408065dd`  
		Last Modified: Tue, 03 Feb 2026 06:02:59 GMT  
		Size: 122.7 MB (122662629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61796f50ec62726694a165792a31ce33d49685d04549abf60827f033df5ccf43`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f4cfd435be2033a741f33edd4c00fb15b3dea8eb934f880316a2d2dbdbcf2589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3aa99b883df392ee8f8918ebba26b085b5d5258c34d8ab7e89526833fe05c`

```dockerfile
```

-	Layers:
	-	`sha256:aab5d6c9625cefc1fc47c3d31a33ed461bc9e942342f83d5780c3fff98e9074e`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 5.6 MB (5632271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4326dc0654079c60e784576195910e3b78068d72326a0b530a0e87693c589158`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130`

```console
$ docker pull ghost@sha256:3ffcb8f2f1f808806e7a0f694a2b130cd78652a26b4337b33fe7e249ce58665a
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
$ docker pull ghost@sha256:db4c990b507f9063e9e1428ea59867bf39f5ebad42246eb1b17cf00ed8b4ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201754407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71366308fc2caced336681cfa4957cee899317205f37f9c325c0e8dbda1204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:49:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:50:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:44:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:44:11 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 03:44:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 03:45:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 03:45:32 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 03:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 03:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:33 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 03:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66d95167c29e1f4d0399617e49250519defda4aa8ea5919064ab3dbd6f0627`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0393491048e0b5148349736f25b7d015e244fee9ab757ef2b0824dc65f3bb9`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 41.0 MB (40982963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a2dcd5a595e7a3d71eacdb266b1f3057397d8a882e9d5a7e55214ea80a21f`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa087727009d9926282b77e9386998f27b6535e550659c7fc1d4ea3b9a973bd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b419252a0ee203e9bebcd21b87684a2d76438133357d02fe0397715d741fc4`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 1.2 MB (1247602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8b2596b3af8b6296ede9aaf62a9409757108296aa7e91263ec687da5b947f`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 11.6 MB (11554942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad0c0054ec5e4c7b33e2ca938892a3c7c44d785c6b34b4724015c6f8ca5a4`  
		Last Modified: Tue, 03 Feb 2026 03:46:08 GMT  
		Size: 118.0 MB (118023390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecf05c1e84beea5440a8eddc45bc88faf593b42c4021c19b754b870beba47e`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:af1ca98cafd5169ff18998e596fbedcbfec146d9d1f115d1c7ad4f1523e8b512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbfd6c3ff5df35ad558360576ba86f301ae29dbeb1661875b0b512a04dbd002`

```dockerfile
```

-	Layers:
	-	`sha256:9a12d1103a71abb258b1ae91ca81660f943d79371130705776728d5f06314db6`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 5.6 MB (5638448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5c4708c40af9d4081f66718d7a3a3303f1792edf265c44dad507ba7307e406`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm variant v7

```console
$ docker pull ghost@sha256:412a891307603ff60265ff535ca07935cd21449bc3a84f19de4a8d39fb5efe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1a7b0d9b80b754520077c154cc7c122ba490be5c544a64af1f93b87bca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:44:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:44:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:44:23 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:16:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:16:34 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:16:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 05:19:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 05:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:36 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f422e3c8e3483b692ceb6f1d2306cabd7f3e6ecc011ba439e95fce34211d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389e52b4174b3a27b61d3f3aa39018a05e20e68d45fbc464a033a4cc380b19b`  
		Last Modified: Tue, 03 Feb 2026 03:44:36 GMT  
		Size: 37.1 MB (37069744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150d5e1afc02a2e46573c8916f0eef87261b4a20cfcad96622ce25ee34cce0d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c55cc18845c75a0db840e1e7b90ad6aa20cc9a8a465124e98aaca205349c9`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e19cf73ee54c7198a0b4f1cbc75b012a1de3938816e18861de3e9d7064f1a`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 1.2 MB (1214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1584472094f5e70f3cca202c7d7a9a521468469284b06f6952ea8eebb0cc68`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 11.6 MB (11555370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23718c2c85accf68e18880a9fc2553f339ba5bef470759c3eaf601b076ecc60`  
		Last Modified: Tue, 03 Feb 2026 05:20:24 GMT  
		Size: 120.6 MB (120584972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3816c666a0e46bf06d39ff06f7c2085f26641e044563411b9b6b7261a95e9`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:835575588bd50edfbe344e957b632dc775be34fed1b5d23f5d18b6888b2a9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d9ad5efa0023f7877c8f800f52b4d53502da8b14e2a5b4c70f86dc25102bd3`

```dockerfile
```

-	Layers:
	-	`sha256:448479178972e381d44e8ec311fc1dbad068faff364e6abaf16660fbb0052be4`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 5.6 MB (5641227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7f4f119d555f4e4c13abdc6b7f5b3a5527d141dd2eac8c5b34588cf942105c`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2f84ae2826bd5b8c1d62628a9ae141b8daec3ed8196d59ffb35346caa05798d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201644231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6aeb7812b275d2d5c26e0a1e4a15acae571e7e40b279d147254d0974e0a81e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:52:33 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:45 GMT
CMD ["node"]
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 04:02:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:02:33 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 04:02:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 04:03:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 04:03:57 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 04:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 04:03:57 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 04:03:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a57bb448d9d8de948e9dfd590e065bb48b5625f7f3b2357c3d66b0da9385`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5334ad83891f85d8537efda275fb71a38a0ada55de771b01c808696232729e0`  
		Last Modified: Tue, 03 Feb 2026 02:53:00 GMT  
		Size: 40.9 MB (40939901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731fb92622470b249c590dc9989be6eaa305251fcb1a5b10ca39d4dcc1c865e`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 1.7 MB (1712602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ce91b8c1d5319a42f2216f1f01ef2aa9546df8ff67be5359146ef34bed80d`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8ef36ef2eb0f9eed5827f821270c37843c518a42bc56b3a79f1029634934c`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 1.2 MB (1201482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf275a028303067f8f30d7cc4598944fcf23ba7d09fddac9f2fdebe5b60c933`  
		Last Modified: Tue, 03 Feb 2026 04:04:32 GMT  
		Size: 11.6 MB (11555247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049cccc3badf5abca466e8eac954fe22a63b2bb1059b35bdf3d9ab817010b443`  
		Last Modified: Tue, 03 Feb 2026 04:04:34 GMT  
		Size: 118.1 MB (118122845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b57f2b897d4abdacaae87cf7f2ae379e429eab83a84b7ee7317e2464a149c9`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:a1dd5d32fd09cd6c374c9a0537eddb7362a8ac0d359531c1f1fc385f8f54b74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608cb4c6896bdc5c6c8b5c8f70af50f44802a29ad5166812884fad2c0903a05`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbeea38fc4479a758bc51cc76900eee05586652212af68be415386c9857c43`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 5.6 MB (5638775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26afdb16f65877a6886579fc0b3cd0e829c498231c0b55d41376ee58fdd26f1b`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; s390x

```console
$ docker pull ghost@sha256:c8144f93af0dd291877d9de1c84a2fa04cc34bb0f9b106ae8d2bdd03e050d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205275425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2fb5c654eaa45e3f6baea2602d5b37d7da9f8bc36c8cef0faf46db2bbdc0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:49:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:51:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:52:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:52:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:59:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:59:31 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:59:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 06:02:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 06:02:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 06:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 06:02:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 06:02:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466ebe0ea905076601b8793254dc31d06b3c76b4d8c4bc3b3053cea0110fb4`  
		Last Modified: Tue, 03 Feb 2026 03:50:01 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5fee3e4eaedf9ac67494a71ce92d031c95788c11ee7afbcdaf7611ca00c50`  
		Last Modified: Tue, 03 Feb 2026 03:52:24 GMT  
		Size: 41.2 MB (41234983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee9d0b0428acaedd477f0aa13962b11044dccc937b415940e62ddc3eb61910`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 1.7 MB (1712656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761b4060e7745b76cc6769879475967fb0a6111ca136ed952547976e3982017`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f344302285e0a2d20bb95d612920aae7161c801d09c78a90390d5f8c3a973`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 1.2 MB (1221387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fdcc29d6fa001a8fd40b696cd24ca5743a566a8386eabe882234198ff7a17`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 11.6 MB (11555055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce51c47940052e76b56be3d3b5a54ffba7b2918aab72497a00815408065dd`  
		Last Modified: Tue, 03 Feb 2026 06:02:59 GMT  
		Size: 122.7 MB (122662629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61796f50ec62726694a165792a31ce33d49685d04549abf60827f033df5ccf43`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:f4cfd435be2033a741f33edd4c00fb15b3dea8eb934f880316a2d2dbdbcf2589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3aa99b883df392ee8f8918ebba26b085b5d5258c34d8ab7e89526833fe05c`

```dockerfile
```

-	Layers:
	-	`sha256:aab5d6c9625cefc1fc47c3d31a33ed461bc9e942342f83d5780c3fff98e9074e`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 5.6 MB (5632271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4326dc0654079c60e784576195910e3b78068d72326a0b530a0e87693c589158`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine`

```console
$ docker pull ghost@sha256:a0506f3f05f5bdc6c950c5113cdcdb1e1f96fbf15f6dc0a39fc093c25348bdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:2341e27e1f3f8496f677f77d0620c1d514e2f4111708bbc03e8bc7c9d39a36fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176143724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e42e1a27813280c68141d3b31ee65c5c729991780f12368265d3615a49db2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:46 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:31:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:49 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:48:42 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:49:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:49:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:49:53 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:49:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:49:54 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:49:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d96c196e3198e14ea37df8bba4f54bf92fb525eb65e49fa4027c7dee13f80`  
		Last Modified: Wed, 28 Jan 2026 03:32:03 GMT  
		Size: 42.8 MB (42782769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87f4721c91769ed5206f34a9ab6ec98fc1d5235c12c2fc956665b1155e9ecb`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 1.3 MB (1262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31b2016552274339ed88ed4a438d78bf37e0f6bdf328d02207b2a598c1ef86d`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a106b9634effefe3ddbf2725d5e37a5fb2edb5e62e7d4a88e76158a4e2abf08`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 821.9 KB (821902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a0aaa90ef05be2fd9a6b377ddd409cbc2f1e843317c63a56495971394db3`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 928.3 KB (928325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97ac866edba5d8600572c2a8389a73fc66e6a385fd4cdf361943c6dfd5d5153`  
		Last Modified: Sun, 01 Feb 2026 07:50:25 GMT  
		Size: 11.6 MB (11579070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32fa910c76f8d8d715c5009b6fa028af53efa371e036e4d44937d8f9ac183a`  
		Last Modified: Sun, 01 Feb 2026 07:50:27 GMT  
		Size: 114.9 MB (114906695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d67e8a832c42b678355b580b89c275badc50789b2ea15430a0b88b1d99a2c`  
		Last Modified: Sun, 01 Feb 2026 07:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06a707175e55a16a6c1c2e4d6a38e86a58afcf312e2f091bfd90f971d304d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56188cd2919f3be565558fb22e57d214985876a4ce7b6957051f08cafcc37e99`

```dockerfile
```

-	Layers:
	-	`sha256:708bd681f03f1f02a74465d20e6d7dec4f9c997af10cbd320f990166a658ad88`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 3.4 MB (3425676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b3739c1900fa76d1e054ec85a8f05443844de716a5f43a652d5b459b045011`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:acd876f9ac707349b5f43fb3a3ec675f904d6d49d2e8db812b6a90c9c163ae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578900d1d08bdebdb3e3097c0141be06de6a868b626ff3817b707002ff826f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:38:48 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:38:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:48 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:38:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:38:51 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:53:35 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:53:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:55:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:55:12 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:55:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:55:12 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:55:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb920e5d251bfb3a5bac54cb1ee6be01e588068fecdf867141fb05734cd3df8`  
		Last Modified: Wed, 28 Jan 2026 03:39:05 GMT  
		Size: 43.1 MB (43121286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e17969cb2d3834a243108c5903feec6ca60dc3607b03867527e15914e86f6a`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d38c2ed5610a9544ddba1a8feb24733822e5c9409816c26c858d2a270efa7`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112be90c7b1dd2681312ed79d221f223ed46b135256091c4d3a99915ef5744b4`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 891.3 KB (891312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a903efa9ccd32343996cb58aaae2cb6e32f11173d18b3926546670ebaae6b9`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 881.3 KB (881297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92085bba5cf6d1a5c82fb89e5588a678313f3885f83cae6b791c9a8d6c7dc40`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 11.6 MB (11580799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb5a1af78d27870aa99a61809a908a85c8dc5d8164ec80e3e2550498714e0f`  
		Last Modified: Sun, 01 Feb 2026 07:55:49 GMT  
		Size: 125.4 MB (125419264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a916ea2e7c6d7950663e4539112347c987bb9902473c56df80589b4ca77f52`  
		Last Modified: Sun, 01 Feb 2026 07:55:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:704554090da3b5a05719f458094167d96eab2a7641e06c81f9bba913cf4f27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5bd03afee28985b232ade1d38440e59782e2fd2bc56cb125fa688d6fbe69b`

```dockerfile
```

-	Layers:
	-	`sha256:72074f0637949691651a4ba1a2fcb6bde15344ef2aa0a06ec73071d862f3b6a0`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 3.4 MB (3425158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8237d498768cfe460a2674de812a5ce8956474f52e7ee6e364d84c68b94d14fa`  
		Last Modified: Sun, 01 Feb 2026 07:55:46 GMT  
		Size: 26.0 KB (25967 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine3.23`

```console
$ docker pull ghost@sha256:a0506f3f05f5bdc6c950c5113cdcdb1e1f96fbf15f6dc0a39fc093c25348bdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:2341e27e1f3f8496f677f77d0620c1d514e2f4111708bbc03e8bc7c9d39a36fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176143724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e42e1a27813280c68141d3b31ee65c5c729991780f12368265d3615a49db2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:46 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:31:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:49 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:48:42 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:49:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:49:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:49:53 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:49:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:49:54 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:49:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d96c196e3198e14ea37df8bba4f54bf92fb525eb65e49fa4027c7dee13f80`  
		Last Modified: Wed, 28 Jan 2026 03:32:03 GMT  
		Size: 42.8 MB (42782769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87f4721c91769ed5206f34a9ab6ec98fc1d5235c12c2fc956665b1155e9ecb`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 1.3 MB (1262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31b2016552274339ed88ed4a438d78bf37e0f6bdf328d02207b2a598c1ef86d`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a106b9634effefe3ddbf2725d5e37a5fb2edb5e62e7d4a88e76158a4e2abf08`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 821.9 KB (821902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a0aaa90ef05be2fd9a6b377ddd409cbc2f1e843317c63a56495971394db3`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 928.3 KB (928325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97ac866edba5d8600572c2a8389a73fc66e6a385fd4cdf361943c6dfd5d5153`  
		Last Modified: Sun, 01 Feb 2026 07:50:25 GMT  
		Size: 11.6 MB (11579070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32fa910c76f8d8d715c5009b6fa028af53efa371e036e4d44937d8f9ac183a`  
		Last Modified: Sun, 01 Feb 2026 07:50:27 GMT  
		Size: 114.9 MB (114906695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d67e8a832c42b678355b580b89c275badc50789b2ea15430a0b88b1d99a2c`  
		Last Modified: Sun, 01 Feb 2026 07:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:06a707175e55a16a6c1c2e4d6a38e86a58afcf312e2f091bfd90f971d304d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56188cd2919f3be565558fb22e57d214985876a4ce7b6957051f08cafcc37e99`

```dockerfile
```

-	Layers:
	-	`sha256:708bd681f03f1f02a74465d20e6d7dec4f9c997af10cbd320f990166a658ad88`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 3.4 MB (3425676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b3739c1900fa76d1e054ec85a8f05443844de716a5f43a652d5b459b045011`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:acd876f9ac707349b5f43fb3a3ec675f904d6d49d2e8db812b6a90c9c163ae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578900d1d08bdebdb3e3097c0141be06de6a868b626ff3817b707002ff826f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:38:48 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:38:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:48 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:38:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:38:51 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:53:35 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:53:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:55:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:55:12 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:55:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:55:12 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:55:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb920e5d251bfb3a5bac54cb1ee6be01e588068fecdf867141fb05734cd3df8`  
		Last Modified: Wed, 28 Jan 2026 03:39:05 GMT  
		Size: 43.1 MB (43121286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e17969cb2d3834a243108c5903feec6ca60dc3607b03867527e15914e86f6a`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d38c2ed5610a9544ddba1a8feb24733822e5c9409816c26c858d2a270efa7`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112be90c7b1dd2681312ed79d221f223ed46b135256091c4d3a99915ef5744b4`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 891.3 KB (891312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a903efa9ccd32343996cb58aaae2cb6e32f11173d18b3926546670ebaae6b9`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 881.3 KB (881297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92085bba5cf6d1a5c82fb89e5588a678313f3885f83cae6b791c9a8d6c7dc40`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 11.6 MB (11580799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb5a1af78d27870aa99a61809a908a85c8dc5d8164ec80e3e2550498714e0f`  
		Last Modified: Sun, 01 Feb 2026 07:55:49 GMT  
		Size: 125.4 MB (125419264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a916ea2e7c6d7950663e4539112347c987bb9902473c56df80589b4ca77f52`  
		Last Modified: Sun, 01 Feb 2026 07:55:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:704554090da3b5a05719f458094167d96eab2a7641e06c81f9bba913cf4f27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5bd03afee28985b232ade1d38440e59782e2fd2bc56cb125fa688d6fbe69b`

```dockerfile
```

-	Layers:
	-	`sha256:72074f0637949691651a4ba1a2fcb6bde15344ef2aa0a06ec73071d862f3b6a0`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 3.4 MB (3425158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8237d498768cfe460a2674de812a5ce8956474f52e7ee6e364d84c68b94d14fa`  
		Last Modified: Sun, 01 Feb 2026 07:55:46 GMT  
		Size: 26.0 KB (25967 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-bookworm`

```console
$ docker pull ghost@sha256:3ffcb8f2f1f808806e7a0f694a2b130cd78652a26b4337b33fe7e249ce58665a
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
$ docker pull ghost@sha256:db4c990b507f9063e9e1428ea59867bf39f5ebad42246eb1b17cf00ed8b4ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201754407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71366308fc2caced336681cfa4957cee899317205f37f9c325c0e8dbda1204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:49:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:50:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:44:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:44:11 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 03:44:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 03:45:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 03:45:32 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 03:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 03:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:33 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 03:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66d95167c29e1f4d0399617e49250519defda4aa8ea5919064ab3dbd6f0627`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0393491048e0b5148349736f25b7d015e244fee9ab757ef2b0824dc65f3bb9`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 41.0 MB (40982963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a2dcd5a595e7a3d71eacdb266b1f3057397d8a882e9d5a7e55214ea80a21f`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa087727009d9926282b77e9386998f27b6535e550659c7fc1d4ea3b9a973bd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b419252a0ee203e9bebcd21b87684a2d76438133357d02fe0397715d741fc4`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 1.2 MB (1247602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8b2596b3af8b6296ede9aaf62a9409757108296aa7e91263ec687da5b947f`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 11.6 MB (11554942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad0c0054ec5e4c7b33e2ca938892a3c7c44d785c6b34b4724015c6f8ca5a4`  
		Last Modified: Tue, 03 Feb 2026 03:46:08 GMT  
		Size: 118.0 MB (118023390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecf05c1e84beea5440a8eddc45bc88faf593b42c4021c19b754b870beba47e`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:af1ca98cafd5169ff18998e596fbedcbfec146d9d1f115d1c7ad4f1523e8b512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbfd6c3ff5df35ad558360576ba86f301ae29dbeb1661875b0b512a04dbd002`

```dockerfile
```

-	Layers:
	-	`sha256:9a12d1103a71abb258b1ae91ca81660f943d79371130705776728d5f06314db6`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 5.6 MB (5638448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5c4708c40af9d4081f66718d7a3a3303f1792edf265c44dad507ba7307e406`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:412a891307603ff60265ff535ca07935cd21449bc3a84f19de4a8d39fb5efe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1a7b0d9b80b754520077c154cc7c122ba490be5c544a64af1f93b87bca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:44:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:44:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:44:23 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:16:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:16:34 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:16:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 05:19:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 05:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:36 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f422e3c8e3483b692ceb6f1d2306cabd7f3e6ecc011ba439e95fce34211d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389e52b4174b3a27b61d3f3aa39018a05e20e68d45fbc464a033a4cc380b19b`  
		Last Modified: Tue, 03 Feb 2026 03:44:36 GMT  
		Size: 37.1 MB (37069744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150d5e1afc02a2e46573c8916f0eef87261b4a20cfcad96622ce25ee34cce0d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c55cc18845c75a0db840e1e7b90ad6aa20cc9a8a465124e98aaca205349c9`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e19cf73ee54c7198a0b4f1cbc75b012a1de3938816e18861de3e9d7064f1a`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 1.2 MB (1214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1584472094f5e70f3cca202c7d7a9a521468469284b06f6952ea8eebb0cc68`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 11.6 MB (11555370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23718c2c85accf68e18880a9fc2553f339ba5bef470759c3eaf601b076ecc60`  
		Last Modified: Tue, 03 Feb 2026 05:20:24 GMT  
		Size: 120.6 MB (120584972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3816c666a0e46bf06d39ff06f7c2085f26641e044563411b9b6b7261a95e9`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:835575588bd50edfbe344e957b632dc775be34fed1b5d23f5d18b6888b2a9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d9ad5efa0023f7877c8f800f52b4d53502da8b14e2a5b4c70f86dc25102bd3`

```dockerfile
```

-	Layers:
	-	`sha256:448479178972e381d44e8ec311fc1dbad068faff364e6abaf16660fbb0052be4`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 5.6 MB (5641227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7f4f119d555f4e4c13abdc6b7f5b3a5527d141dd2eac8c5b34588cf942105c`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2f84ae2826bd5b8c1d62628a9ae141b8daec3ed8196d59ffb35346caa05798d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201644231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6aeb7812b275d2d5c26e0a1e4a15acae571e7e40b279d147254d0974e0a81e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:52:33 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:45 GMT
CMD ["node"]
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 04:02:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:02:33 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 04:02:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 04:03:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 04:03:57 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 04:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 04:03:57 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 04:03:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a57bb448d9d8de948e9dfd590e065bb48b5625f7f3b2357c3d66b0da9385`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5334ad83891f85d8537efda275fb71a38a0ada55de771b01c808696232729e0`  
		Last Modified: Tue, 03 Feb 2026 02:53:00 GMT  
		Size: 40.9 MB (40939901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731fb92622470b249c590dc9989be6eaa305251fcb1a5b10ca39d4dcc1c865e`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 1.7 MB (1712602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ce91b8c1d5319a42f2216f1f01ef2aa9546df8ff67be5359146ef34bed80d`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8ef36ef2eb0f9eed5827f821270c37843c518a42bc56b3a79f1029634934c`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 1.2 MB (1201482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf275a028303067f8f30d7cc4598944fcf23ba7d09fddac9f2fdebe5b60c933`  
		Last Modified: Tue, 03 Feb 2026 04:04:32 GMT  
		Size: 11.6 MB (11555247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049cccc3badf5abca466e8eac954fe22a63b2bb1059b35bdf3d9ab817010b443`  
		Last Modified: Tue, 03 Feb 2026 04:04:34 GMT  
		Size: 118.1 MB (118122845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b57f2b897d4abdacaae87cf7f2ae379e429eab83a84b7ee7317e2464a149c9`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a1dd5d32fd09cd6c374c9a0537eddb7362a8ac0d359531c1f1fc385f8f54b74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608cb4c6896bdc5c6c8b5c8f70af50f44802a29ad5166812884fad2c0903a05`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbeea38fc4479a758bc51cc76900eee05586652212af68be415386c9857c43`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 5.6 MB (5638775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26afdb16f65877a6886579fc0b3cd0e829c498231c0b55d41376ee58fdd26f1b`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c8144f93af0dd291877d9de1c84a2fa04cc34bb0f9b106ae8d2bdd03e050d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205275425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2fb5c654eaa45e3f6baea2602d5b37d7da9f8bc36c8cef0faf46db2bbdc0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:49:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:51:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:52:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:52:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:59:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:59:31 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:59:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 06:02:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 06:02:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 06:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 06:02:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 06:02:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466ebe0ea905076601b8793254dc31d06b3c76b4d8c4bc3b3053cea0110fb4`  
		Last Modified: Tue, 03 Feb 2026 03:50:01 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5fee3e4eaedf9ac67494a71ce92d031c95788c11ee7afbcdaf7611ca00c50`  
		Last Modified: Tue, 03 Feb 2026 03:52:24 GMT  
		Size: 41.2 MB (41234983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee9d0b0428acaedd477f0aa13962b11044dccc937b415940e62ddc3eb61910`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 1.7 MB (1712656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761b4060e7745b76cc6769879475967fb0a6111ca136ed952547976e3982017`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f344302285e0a2d20bb95d612920aae7161c801d09c78a90390d5f8c3a973`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 1.2 MB (1221387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fdcc29d6fa001a8fd40b696cd24ca5743a566a8386eabe882234198ff7a17`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 11.6 MB (11555055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce51c47940052e76b56be3d3b5a54ffba7b2918aab72497a00815408065dd`  
		Last Modified: Tue, 03 Feb 2026 06:02:59 GMT  
		Size: 122.7 MB (122662629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61796f50ec62726694a165792a31ce33d49685d04549abf60827f033df5ccf43`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f4cfd435be2033a741f33edd4c00fb15b3dea8eb934f880316a2d2dbdbcf2589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3aa99b883df392ee8f8918ebba26b085b5d5258c34d8ab7e89526833fe05c`

```dockerfile
```

-	Layers:
	-	`sha256:aab5d6c9625cefc1fc47c3d31a33ed461bc9e942342f83d5780c3fff98e9074e`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 5.6 MB (5632271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4326dc0654079c60e784576195910e3b78068d72326a0b530a0e87693c589158`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6`

```console
$ docker pull ghost@sha256:3ffcb8f2f1f808806e7a0f694a2b130cd78652a26b4337b33fe7e249ce58665a
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

### `ghost:5.130.6` - linux; amd64

```console
$ docker pull ghost@sha256:db4c990b507f9063e9e1428ea59867bf39f5ebad42246eb1b17cf00ed8b4ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201754407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71366308fc2caced336681cfa4957cee899317205f37f9c325c0e8dbda1204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:49:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:50:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:44:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:44:11 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 03:44:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 03:45:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 03:45:32 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 03:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 03:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:33 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 03:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66d95167c29e1f4d0399617e49250519defda4aa8ea5919064ab3dbd6f0627`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0393491048e0b5148349736f25b7d015e244fee9ab757ef2b0824dc65f3bb9`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 41.0 MB (40982963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a2dcd5a595e7a3d71eacdb266b1f3057397d8a882e9d5a7e55214ea80a21f`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa087727009d9926282b77e9386998f27b6535e550659c7fc1d4ea3b9a973bd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b419252a0ee203e9bebcd21b87684a2d76438133357d02fe0397715d741fc4`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 1.2 MB (1247602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8b2596b3af8b6296ede9aaf62a9409757108296aa7e91263ec687da5b947f`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 11.6 MB (11554942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad0c0054ec5e4c7b33e2ca938892a3c7c44d785c6b34b4724015c6f8ca5a4`  
		Last Modified: Tue, 03 Feb 2026 03:46:08 GMT  
		Size: 118.0 MB (118023390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecf05c1e84beea5440a8eddc45bc88faf593b42c4021c19b754b870beba47e`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:af1ca98cafd5169ff18998e596fbedcbfec146d9d1f115d1c7ad4f1523e8b512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbfd6c3ff5df35ad558360576ba86f301ae29dbeb1661875b0b512a04dbd002`

```dockerfile
```

-	Layers:
	-	`sha256:9a12d1103a71abb258b1ae91ca81660f943d79371130705776728d5f06314db6`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 5.6 MB (5638448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5c4708c40af9d4081f66718d7a3a3303f1792edf265c44dad507ba7307e406`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:412a891307603ff60265ff535ca07935cd21449bc3a84f19de4a8d39fb5efe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1a7b0d9b80b754520077c154cc7c122ba490be5c544a64af1f93b87bca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:44:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:44:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:44:23 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:16:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:16:34 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:16:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 05:19:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 05:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:36 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f422e3c8e3483b692ceb6f1d2306cabd7f3e6ecc011ba439e95fce34211d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389e52b4174b3a27b61d3f3aa39018a05e20e68d45fbc464a033a4cc380b19b`  
		Last Modified: Tue, 03 Feb 2026 03:44:36 GMT  
		Size: 37.1 MB (37069744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150d5e1afc02a2e46573c8916f0eef87261b4a20cfcad96622ce25ee34cce0d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c55cc18845c75a0db840e1e7b90ad6aa20cc9a8a465124e98aaca205349c9`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e19cf73ee54c7198a0b4f1cbc75b012a1de3938816e18861de3e9d7064f1a`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 1.2 MB (1214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1584472094f5e70f3cca202c7d7a9a521468469284b06f6952ea8eebb0cc68`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 11.6 MB (11555370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23718c2c85accf68e18880a9fc2553f339ba5bef470759c3eaf601b076ecc60`  
		Last Modified: Tue, 03 Feb 2026 05:20:24 GMT  
		Size: 120.6 MB (120584972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3816c666a0e46bf06d39ff06f7c2085f26641e044563411b9b6b7261a95e9`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:835575588bd50edfbe344e957b632dc775be34fed1b5d23f5d18b6888b2a9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d9ad5efa0023f7877c8f800f52b4d53502da8b14e2a5b4c70f86dc25102bd3`

```dockerfile
```

-	Layers:
	-	`sha256:448479178972e381d44e8ec311fc1dbad068faff364e6abaf16660fbb0052be4`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 5.6 MB (5641227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7f4f119d555f4e4c13abdc6b7f5b3a5527d141dd2eac8c5b34588cf942105c`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2f84ae2826bd5b8c1d62628a9ae141b8daec3ed8196d59ffb35346caa05798d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201644231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6aeb7812b275d2d5c26e0a1e4a15acae571e7e40b279d147254d0974e0a81e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:52:33 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:45 GMT
CMD ["node"]
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 04:02:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:02:33 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 04:02:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 04:03:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 04:03:57 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 04:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 04:03:57 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 04:03:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a57bb448d9d8de948e9dfd590e065bb48b5625f7f3b2357c3d66b0da9385`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5334ad83891f85d8537efda275fb71a38a0ada55de771b01c808696232729e0`  
		Last Modified: Tue, 03 Feb 2026 02:53:00 GMT  
		Size: 40.9 MB (40939901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731fb92622470b249c590dc9989be6eaa305251fcb1a5b10ca39d4dcc1c865e`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 1.7 MB (1712602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ce91b8c1d5319a42f2216f1f01ef2aa9546df8ff67be5359146ef34bed80d`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8ef36ef2eb0f9eed5827f821270c37843c518a42bc56b3a79f1029634934c`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 1.2 MB (1201482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf275a028303067f8f30d7cc4598944fcf23ba7d09fddac9f2fdebe5b60c933`  
		Last Modified: Tue, 03 Feb 2026 04:04:32 GMT  
		Size: 11.6 MB (11555247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049cccc3badf5abca466e8eac954fe22a63b2bb1059b35bdf3d9ab817010b443`  
		Last Modified: Tue, 03 Feb 2026 04:04:34 GMT  
		Size: 118.1 MB (118122845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b57f2b897d4abdacaae87cf7f2ae379e429eab83a84b7ee7317e2464a149c9`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:a1dd5d32fd09cd6c374c9a0537eddb7362a8ac0d359531c1f1fc385f8f54b74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608cb4c6896bdc5c6c8b5c8f70af50f44802a29ad5166812884fad2c0903a05`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbeea38fc4479a758bc51cc76900eee05586652212af68be415386c9857c43`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 5.6 MB (5638775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26afdb16f65877a6886579fc0b3cd0e829c498231c0b55d41376ee58fdd26f1b`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6` - linux; s390x

```console
$ docker pull ghost@sha256:c8144f93af0dd291877d9de1c84a2fa04cc34bb0f9b106ae8d2bdd03e050d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205275425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2fb5c654eaa45e3f6baea2602d5b37d7da9f8bc36c8cef0faf46db2bbdc0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:49:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:51:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:52:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:52:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:59:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:59:31 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:59:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 06:02:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 06:02:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 06:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 06:02:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 06:02:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466ebe0ea905076601b8793254dc31d06b3c76b4d8c4bc3b3053cea0110fb4`  
		Last Modified: Tue, 03 Feb 2026 03:50:01 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5fee3e4eaedf9ac67494a71ce92d031c95788c11ee7afbcdaf7611ca00c50`  
		Last Modified: Tue, 03 Feb 2026 03:52:24 GMT  
		Size: 41.2 MB (41234983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee9d0b0428acaedd477f0aa13962b11044dccc937b415940e62ddc3eb61910`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 1.7 MB (1712656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761b4060e7745b76cc6769879475967fb0a6111ca136ed952547976e3982017`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f344302285e0a2d20bb95d612920aae7161c801d09c78a90390d5f8c3a973`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 1.2 MB (1221387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fdcc29d6fa001a8fd40b696cd24ca5743a566a8386eabe882234198ff7a17`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 11.6 MB (11555055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce51c47940052e76b56be3d3b5a54ffba7b2918aab72497a00815408065dd`  
		Last Modified: Tue, 03 Feb 2026 06:02:59 GMT  
		Size: 122.7 MB (122662629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61796f50ec62726694a165792a31ce33d49685d04549abf60827f033df5ccf43`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:f4cfd435be2033a741f33edd4c00fb15b3dea8eb934f880316a2d2dbdbcf2589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3aa99b883df392ee8f8918ebba26b085b5d5258c34d8ab7e89526833fe05c`

```dockerfile
```

-	Layers:
	-	`sha256:aab5d6c9625cefc1fc47c3d31a33ed461bc9e942342f83d5780c3fff98e9074e`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 5.6 MB (5632271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4326dc0654079c60e784576195910e3b78068d72326a0b530a0e87693c589158`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6-alpine`

```console
$ docker pull ghost@sha256:a0506f3f05f5bdc6c950c5113cdcdb1e1f96fbf15f6dc0a39fc093c25348bdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:2341e27e1f3f8496f677f77d0620c1d514e2f4111708bbc03e8bc7c9d39a36fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176143724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e42e1a27813280c68141d3b31ee65c5c729991780f12368265d3615a49db2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:46 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:31:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:49 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:48:42 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:49:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:49:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:49:53 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:49:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:49:54 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:49:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d96c196e3198e14ea37df8bba4f54bf92fb525eb65e49fa4027c7dee13f80`  
		Last Modified: Wed, 28 Jan 2026 03:32:03 GMT  
		Size: 42.8 MB (42782769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87f4721c91769ed5206f34a9ab6ec98fc1d5235c12c2fc956665b1155e9ecb`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 1.3 MB (1262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31b2016552274339ed88ed4a438d78bf37e0f6bdf328d02207b2a598c1ef86d`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a106b9634effefe3ddbf2725d5e37a5fb2edb5e62e7d4a88e76158a4e2abf08`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 821.9 KB (821902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a0aaa90ef05be2fd9a6b377ddd409cbc2f1e843317c63a56495971394db3`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 928.3 KB (928325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97ac866edba5d8600572c2a8389a73fc66e6a385fd4cdf361943c6dfd5d5153`  
		Last Modified: Sun, 01 Feb 2026 07:50:25 GMT  
		Size: 11.6 MB (11579070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32fa910c76f8d8d715c5009b6fa028af53efa371e036e4d44937d8f9ac183a`  
		Last Modified: Sun, 01 Feb 2026 07:50:27 GMT  
		Size: 114.9 MB (114906695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d67e8a832c42b678355b580b89c275badc50789b2ea15430a0b88b1d99a2c`  
		Last Modified: Sun, 01 Feb 2026 07:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:06a707175e55a16a6c1c2e4d6a38e86a58afcf312e2f091bfd90f971d304d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56188cd2919f3be565558fb22e57d214985876a4ce7b6957051f08cafcc37e99`

```dockerfile
```

-	Layers:
	-	`sha256:708bd681f03f1f02a74465d20e6d7dec4f9c997af10cbd320f990166a658ad88`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 3.4 MB (3425676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b3739c1900fa76d1e054ec85a8f05443844de716a5f43a652d5b459b045011`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:acd876f9ac707349b5f43fb3a3ec675f904d6d49d2e8db812b6a90c9c163ae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578900d1d08bdebdb3e3097c0141be06de6a868b626ff3817b707002ff826f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:38:48 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:38:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:48 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:38:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:38:51 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:53:35 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:53:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:55:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:55:12 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:55:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:55:12 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:55:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb920e5d251bfb3a5bac54cb1ee6be01e588068fecdf867141fb05734cd3df8`  
		Last Modified: Wed, 28 Jan 2026 03:39:05 GMT  
		Size: 43.1 MB (43121286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e17969cb2d3834a243108c5903feec6ca60dc3607b03867527e15914e86f6a`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d38c2ed5610a9544ddba1a8feb24733822e5c9409816c26c858d2a270efa7`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112be90c7b1dd2681312ed79d221f223ed46b135256091c4d3a99915ef5744b4`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 891.3 KB (891312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a903efa9ccd32343996cb58aaae2cb6e32f11173d18b3926546670ebaae6b9`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 881.3 KB (881297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92085bba5cf6d1a5c82fb89e5588a678313f3885f83cae6b791c9a8d6c7dc40`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 11.6 MB (11580799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb5a1af78d27870aa99a61809a908a85c8dc5d8164ec80e3e2550498714e0f`  
		Last Modified: Sun, 01 Feb 2026 07:55:49 GMT  
		Size: 125.4 MB (125419264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a916ea2e7c6d7950663e4539112347c987bb9902473c56df80589b4ca77f52`  
		Last Modified: Sun, 01 Feb 2026 07:55:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:704554090da3b5a05719f458094167d96eab2a7641e06c81f9bba913cf4f27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5bd03afee28985b232ade1d38440e59782e2fd2bc56cb125fa688d6fbe69b`

```dockerfile
```

-	Layers:
	-	`sha256:72074f0637949691651a4ba1a2fcb6bde15344ef2aa0a06ec73071d862f3b6a0`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 3.4 MB (3425158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8237d498768cfe460a2674de812a5ce8956474f52e7ee6e364d84c68b94d14fa`  
		Last Modified: Sun, 01 Feb 2026 07:55:46 GMT  
		Size: 26.0 KB (25967 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6-alpine3.23`

```console
$ docker pull ghost@sha256:a0506f3f05f5bdc6c950c5113cdcdb1e1f96fbf15f6dc0a39fc093c25348bdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:2341e27e1f3f8496f677f77d0620c1d514e2f4111708bbc03e8bc7c9d39a36fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176143724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e42e1a27813280c68141d3b31ee65c5c729991780f12368265d3615a49db2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:46 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:31:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:49 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:48:42 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:48:46 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:48:46 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:49:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:49:00 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:49:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:49:53 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:49:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:49:54 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:49:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d96c196e3198e14ea37df8bba4f54bf92fb525eb65e49fa4027c7dee13f80`  
		Last Modified: Wed, 28 Jan 2026 03:32:03 GMT  
		Size: 42.8 MB (42782769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87f4721c91769ed5206f34a9ab6ec98fc1d5235c12c2fc956665b1155e9ecb`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 1.3 MB (1262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31b2016552274339ed88ed4a438d78bf37e0f6bdf328d02207b2a598c1ef86d`  
		Last Modified: Wed, 28 Jan 2026 03:32:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a106b9634effefe3ddbf2725d5e37a5fb2edb5e62e7d4a88e76158a4e2abf08`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 821.9 KB (821902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a0aaa90ef05be2fd9a6b377ddd409cbc2f1e843317c63a56495971394db3`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 928.3 KB (928325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97ac866edba5d8600572c2a8389a73fc66e6a385fd4cdf361943c6dfd5d5153`  
		Last Modified: Sun, 01 Feb 2026 07:50:25 GMT  
		Size: 11.6 MB (11579070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32fa910c76f8d8d715c5009b6fa028af53efa371e036e4d44937d8f9ac183a`  
		Last Modified: Sun, 01 Feb 2026 07:50:27 GMT  
		Size: 114.9 MB (114906695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d67e8a832c42b678355b580b89c275badc50789b2ea15430a0b88b1d99a2c`  
		Last Modified: Sun, 01 Feb 2026 07:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:06a707175e55a16a6c1c2e4d6a38e86a58afcf312e2f091bfd90f971d304d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56188cd2919f3be565558fb22e57d214985876a4ce7b6957051f08cafcc37e99`

```dockerfile
```

-	Layers:
	-	`sha256:708bd681f03f1f02a74465d20e6d7dec4f9c997af10cbd320f990166a658ad88`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 3.4 MB (3425676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b3739c1900fa76d1e054ec85a8f05443844de716a5f43a652d5b459b045011`  
		Last Modified: Sun, 01 Feb 2026 07:50:24 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:acd876f9ac707349b5f43fb3a3ec675f904d6d49d2e8db812b6a90c9c163ae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578900d1d08bdebdb3e3097c0141be06de6a868b626ff3817b707002ff826f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:38:48 GMT
ENV NODE_VERSION=20.20.0
# Wed, 28 Jan 2026 03:38:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:48 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:38:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:38:51 GMT
CMD ["node"]
# Sun, 01 Feb 2026 07:53:35 GMT
RUN apk add --no-cache 		bash # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:39 GMT
ENV NODE_ENV=production
# Sun, 01 Feb 2026 07:53:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Sun, 01 Feb 2026 07:53:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 01 Feb 2026 07:53:55 GMT
ENV GHOST_VERSION=5.130.6
# Sun, 01 Feb 2026 07:55:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
WORKDIR /var/lib/ghost
# Sun, 01 Feb 2026 07:55:12 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 01 Feb 2026 07:55:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 07:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 07:55:12 GMT
EXPOSE map[2368/tcp:{}]
# Sun, 01 Feb 2026 07:55:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb920e5d251bfb3a5bac54cb1ee6be01e588068fecdf867141fb05734cd3df8`  
		Last Modified: Wed, 28 Jan 2026 03:39:05 GMT  
		Size: 43.1 MB (43121286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e17969cb2d3834a243108c5903feec6ca60dc3607b03867527e15914e86f6a`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d38c2ed5610a9544ddba1a8feb24733822e5c9409816c26c858d2a270efa7`  
		Last Modified: Wed, 28 Jan 2026 03:39:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112be90c7b1dd2681312ed79d221f223ed46b135256091c4d3a99915ef5744b4`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 891.3 KB (891312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a903efa9ccd32343996cb58aaae2cb6e32f11173d18b3926546670ebaae6b9`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 881.3 KB (881297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92085bba5cf6d1a5c82fb89e5588a678313f3885f83cae6b791c9a8d6c7dc40`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 11.6 MB (11580799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb5a1af78d27870aa99a61809a908a85c8dc5d8164ec80e3e2550498714e0f`  
		Last Modified: Sun, 01 Feb 2026 07:55:49 GMT  
		Size: 125.4 MB (125419264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a916ea2e7c6d7950663e4539112347c987bb9902473c56df80589b4ca77f52`  
		Last Modified: Sun, 01 Feb 2026 07:55:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:704554090da3b5a05719f458094167d96eab2a7641e06c81f9bba913cf4f27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3451125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5bd03afee28985b232ade1d38440e59782e2fd2bc56cb125fa688d6fbe69b`

```dockerfile
```

-	Layers:
	-	`sha256:72074f0637949691651a4ba1a2fcb6bde15344ef2aa0a06ec73071d862f3b6a0`  
		Last Modified: Sun, 01 Feb 2026 07:55:47 GMT  
		Size: 3.4 MB (3425158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8237d498768cfe460a2674de812a5ce8956474f52e7ee6e364d84c68b94d14fa`  
		Last Modified: Sun, 01 Feb 2026 07:55:46 GMT  
		Size: 26.0 KB (25967 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6-bookworm`

```console
$ docker pull ghost@sha256:3ffcb8f2f1f808806e7a0f694a2b130cd78652a26b4337b33fe7e249ce58665a
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

### `ghost:5.130.6-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:db4c990b507f9063e9e1428ea59867bf39f5ebad42246eb1b17cf00ed8b4ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201754407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71366308fc2caced336681cfa4957cee899317205f37f9c325c0e8dbda1204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:49:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:48 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:50:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:44:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:44:11 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 03:44:11 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 03:44:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 03:44:26 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 03:45:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 03:45:32 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 03:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 03:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:33 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 03:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66d95167c29e1f4d0399617e49250519defda4aa8ea5919064ab3dbd6f0627`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0393491048e0b5148349736f25b7d015e244fee9ab757ef2b0824dc65f3bb9`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 41.0 MB (40982963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a2dcd5a595e7a3d71eacdb266b1f3057397d8a882e9d5a7e55214ea80a21f`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa087727009d9926282b77e9386998f27b6535e550659c7fc1d4ea3b9a973bd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b419252a0ee203e9bebcd21b87684a2d76438133357d02fe0397715d741fc4`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 1.2 MB (1247602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8b2596b3af8b6296ede9aaf62a9409757108296aa7e91263ec687da5b947f`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 11.6 MB (11554942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad0c0054ec5e4c7b33e2ca938892a3c7c44d785c6b34b4724015c6f8ca5a4`  
		Last Modified: Tue, 03 Feb 2026 03:46:08 GMT  
		Size: 118.0 MB (118023390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecf05c1e84beea5440a8eddc45bc88faf593b42c4021c19b754b870beba47e`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:af1ca98cafd5169ff18998e596fbedcbfec146d9d1f115d1c7ad4f1523e8b512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbfd6c3ff5df35ad558360576ba86f301ae29dbeb1661875b0b512a04dbd002`

```dockerfile
```

-	Layers:
	-	`sha256:9a12d1103a71abb258b1ae91ca81660f943d79371130705776728d5f06314db6`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 5.6 MB (5638448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5c4708c40af9d4081f66718d7a3a3303f1792edf265c44dad507ba7307e406`  
		Last Modified: Tue, 03 Feb 2026 03:46:05 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:412a891307603ff60265ff535ca07935cd21449bc3a84f19de4a8d39fb5efe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1a7b0d9b80b754520077c154cc7c122ba490be5c544a64af1f93b87bca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:44:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:09 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:44:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:44:23 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:16:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:16:34 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:16:34 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:16:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:16:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 05:19:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 05:19:36 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 05:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:36 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 05:19:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f422e3c8e3483b692ceb6f1d2306cabd7f3e6ecc011ba439e95fce34211d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389e52b4174b3a27b61d3f3aa39018a05e20e68d45fbc464a033a4cc380b19b`  
		Last Modified: Tue, 03 Feb 2026 03:44:36 GMT  
		Size: 37.1 MB (37069744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150d5e1afc02a2e46573c8916f0eef87261b4a20cfcad96622ce25ee34cce0d`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c55cc18845c75a0db840e1e7b90ad6aa20cc9a8a465124e98aaca205349c9`  
		Last Modified: Tue, 03 Feb 2026 03:44:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e19cf73ee54c7198a0b4f1cbc75b012a1de3938816e18861de3e9d7064f1a`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 1.2 MB (1214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1584472094f5e70f3cca202c7d7a9a521468469284b06f6952ea8eebb0cc68`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 11.6 MB (11555370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23718c2c85accf68e18880a9fc2553f339ba5bef470759c3eaf601b076ecc60`  
		Last Modified: Tue, 03 Feb 2026 05:20:24 GMT  
		Size: 120.6 MB (120584972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3816c666a0e46bf06d39ff06f7c2085f26641e044563411b9b6b7261a95e9`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:835575588bd50edfbe344e957b632dc775be34fed1b5d23f5d18b6888b2a9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d9ad5efa0023f7877c8f800f52b4d53502da8b14e2a5b4c70f86dc25102bd3`

```dockerfile
```

-	Layers:
	-	`sha256:448479178972e381d44e8ec311fc1dbad068faff364e6abaf16660fbb0052be4`  
		Last Modified: Tue, 03 Feb 2026 05:20:22 GMT  
		Size: 5.6 MB (5641227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7f4f119d555f4e4c13abdc6b7f5b3a5527d141dd2eac8c5b34588cf942105c`  
		Last Modified: Tue, 03 Feb 2026 05:20:21 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2f84ae2826bd5b8c1d62628a9ae141b8daec3ed8196d59ffb35346caa05798d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201644231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6aeb7812b275d2d5c26e0a1e4a15acae571e7e40b279d147254d0974e0a81e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 02:52:33 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:45 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:45 GMT
CMD ["node"]
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 04:02:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:02:33 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 04:02:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 04:02:46 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 04:02:46 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 04:03:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 04:03:57 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 04:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 04:03:57 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 04:03:57 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a57bb448d9d8de948e9dfd590e065bb48b5625f7f3b2357c3d66b0da9385`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5334ad83891f85d8537efda275fb71a38a0ada55de771b01c808696232729e0`  
		Last Modified: Tue, 03 Feb 2026 02:53:00 GMT  
		Size: 40.9 MB (40939901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731fb92622470b249c590dc9989be6eaa305251fcb1a5b10ca39d4dcc1c865e`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 1.7 MB (1712602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ce91b8c1d5319a42f2216f1f01ef2aa9546df8ff67be5359146ef34bed80d`  
		Last Modified: Tue, 03 Feb 2026 02:52:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8ef36ef2eb0f9eed5827f821270c37843c518a42bc56b3a79f1029634934c`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 1.2 MB (1201482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf275a028303067f8f30d7cc4598944fcf23ba7d09fddac9f2fdebe5b60c933`  
		Last Modified: Tue, 03 Feb 2026 04:04:32 GMT  
		Size: 11.6 MB (11555247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049cccc3badf5abca466e8eac954fe22a63b2bb1059b35bdf3d9ab817010b443`  
		Last Modified: Tue, 03 Feb 2026 04:04:34 GMT  
		Size: 118.1 MB (118122845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b57f2b897d4abdacaae87cf7f2ae379e429eab83a84b7ee7317e2464a149c9`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a1dd5d32fd09cd6c374c9a0537eddb7362a8ac0d359531c1f1fc385f8f54b74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608cb4c6896bdc5c6c8b5c8f70af50f44802a29ad5166812884fad2c0903a05`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbeea38fc4479a758bc51cc76900eee05586652212af68be415386c9857c43`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 5.6 MB (5638775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26afdb16f65877a6886579fc0b3cd0e829c498231c0b55d41376ee58fdd26f1b`  
		Last Modified: Tue, 03 Feb 2026 04:04:31 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c8144f93af0dd291877d9de1c84a2fa04cc34bb0f9b106ae8d2bdd03e050d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205275425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2fb5c654eaa45e3f6baea2602d5b37d7da9f8bc36c8cef0faf46db2bbdc0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:49:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV NODE_VERSION=20.20.0
# Tue, 03 Feb 2026 03:51:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:52:01 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:52:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:52:01 GMT
CMD ["node"]
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:59:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:59:31 GMT
ENV NODE_ENV=production
# Tue, 03 Feb 2026 05:59:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 03 Feb 2026 05:59:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 03 Feb 2026 05:59:47 GMT
ENV GHOST_VERSION=5.130.6
# Tue, 03 Feb 2026 06:02:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
WORKDIR /var/lib/ghost
# Tue, 03 Feb 2026 06:02:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 03 Feb 2026 06:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 06:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 06:02:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 03 Feb 2026 06:02:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466ebe0ea905076601b8793254dc31d06b3c76b4d8c4bc3b3053cea0110fb4`  
		Last Modified: Tue, 03 Feb 2026 03:50:01 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5fee3e4eaedf9ac67494a71ce92d031c95788c11ee7afbcdaf7611ca00c50`  
		Last Modified: Tue, 03 Feb 2026 03:52:24 GMT  
		Size: 41.2 MB (41234983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee9d0b0428acaedd477f0aa13962b11044dccc937b415940e62ddc3eb61910`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 1.7 MB (1712656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761b4060e7745b76cc6769879475967fb0a6111ca136ed952547976e3982017`  
		Last Modified: Tue, 03 Feb 2026 03:52:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f344302285e0a2d20bb95d612920aae7161c801d09c78a90390d5f8c3a973`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 1.2 MB (1221387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fdcc29d6fa001a8fd40b696cd24ca5743a566a8386eabe882234198ff7a17`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 11.6 MB (11555055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce51c47940052e76b56be3d3b5a54ffba7b2918aab72497a00815408065dd`  
		Last Modified: Tue, 03 Feb 2026 06:02:59 GMT  
		Size: 122.7 MB (122662629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61796f50ec62726694a165792a31ce33d49685d04549abf60827f033df5ccf43`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f4cfd435be2033a741f33edd4c00fb15b3dea8eb934f880316a2d2dbdbcf2589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3aa99b883df392ee8f8918ebba26b085b5d5258c34d8ab7e89526833fe05c`

```dockerfile
```

-	Layers:
	-	`sha256:aab5d6c9625cefc1fc47c3d31a33ed461bc9e942342f83d5780c3fff98e9074e`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 5.6 MB (5632271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4326dc0654079c60e784576195910e3b78068d72326a0b530a0e87693c589158`  
		Last Modified: Tue, 03 Feb 2026 06:02:57 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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

### `ghost:6.17` - linux; amd64

```console
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17-alpine`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.17-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17-alpine3.23`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.17-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17-bookworm`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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

### `ghost:6.17-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17.0`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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

### `ghost:6.17.0` - linux; amd64

```console
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17.0-alpine`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.17.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17.0-alpine3.23`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.17.0-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.17.0-bookworm`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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

### `ghost:6.17.0-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.17.0-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.17.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:ea310abfbc90375e1534ba9c394553ab6091a991e0689e3b622675ebb383bc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:9b38c94dfc52973d26b87598d8bed5ec578c7799feeb8e7ac2d3a5df34ca0b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208119837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c68d279ffa35e8e24f8ba7081396a7e526384cff3758fdae0f9abce49d3065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:30:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:30:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:30:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:31:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:31:02 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:55 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:58 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:08 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:08 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:07 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:07 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d513d1f314d3646adaf156be912f8de408c740e43d90cad5ce06b9de27e7bdf`  
		Last Modified: Wed, 28 Jan 2026 03:31:16 GMT  
		Size: 51.6 MB (51601924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b752f7c71fd1a08980fdf09b7379d8304c8ef2569526934a2089ed26d771778`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 1.3 MB (1262117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c5222d85fe45cd255019912158424888b168c8413fb42c8e166c37f1833eb`  
		Last Modified: Wed, 28 Jan 2026 03:31:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90845490f4c7f8fe6086e22be6ff46dd360695c276f03fecb8085729522503`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 821.9 KB (821905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674b530452e23e6a4092b815a1880d15bd3b6ef77c18ed3aee781dfc2037fb8`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 928.3 KB (928329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba732e19e0336f7bfd371df68330208c82f9cff78bd4e327d219f2bed9c31f`  
		Last Modified: Thu, 05 Feb 2026 23:10:43 GMT  
		Size: 12.1 MB (12138139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff24a055d6483084f951dca58308f3bbb87d676c1a089765361125c60ddb034`  
		Last Modified: Thu, 05 Feb 2026 23:10:45 GMT  
		Size: 137.5 MB (137504581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb8342f1c48beaa31777c6470c3858e0809a561b40d6084e2007008476a29d`  
		Last Modified: Thu, 05 Feb 2026 23:10:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c1ac5d838021f698e8ae74750d31c531b458cf5778575fe7b615c325d79054ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8736418667f780e913d8b8815d9395f1719052519166348b20e68b40056f3`

```dockerfile
```

-	Layers:
	-	`sha256:ed9dafd7f7545dedc5bcd41a0ff09385957d75ba3e2e5e36c8d07abad99e8eea`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 3.5 MB (3487132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa108348a2789dff1d42d3dace351deee35f23ad7c2c89f3c93d160b890cc82`  
		Last Modified: Thu, 05 Feb 2026 23:10:42 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cf058d8151f8c64394f689c69d8eceef85b2cc9667eff01472432cca3c6d3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219996211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b3ef3b95dab4ef8fcdbfacb1d21b68e6041bf86c982019760e08d977421c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:54 GMT
ENV NODE_VERSION=22.22.0
# Wed, 28 Jan 2026 03:46:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 28 Jan 2026 03:46:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:46:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:06 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:09 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:22 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:58 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:58 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088de1f599b117d4fd7d0109d786f2f3c2a8e74b063a11730c106ea3c795cb6`  
		Last Modified: Wed, 28 Jan 2026 03:47:14 GMT  
		Size: 52.2 MB (52237572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691184ba0a570957c383fb80dd573d665b8d320f9e4a8168e6dd18c5e702c0c`  
		Last Modified: Wed, 28 Jan 2026 03:47:13 GMT  
		Size: 1.3 MB (1262990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558f33bb3b6e9c80d4c77bec5c801380ee995c9c4a2ac331712725f5e7b5509`  
		Last Modified: Wed, 28 Jan 2026 03:47:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751e8f6e610f7e885c1d499ea5d9c0c3206f2f76411b16fdfd1ff461a92a989`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 891.3 KB (891300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20636b7c373f96523f3af68fe0bb912e2627b04c6c295595627ec9afa05068`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501ffe0e58793f243f05c36c820b3da80261e50f19d1d9371b6a6e43ddec02b`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 12.1 MB (12138466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b296e53aa0609b147298e6fb795381fc45040263f303c62ff6cd0b8cc2ce8b6`  
		Last Modified: Thu, 05 Feb 2026 23:12:41 GMT  
		Size: 148.4 MB (148386483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa319a6bd74f9f37835813f199111098454966c49667ffb649081772ca4427cb`  
		Last Modified: Thu, 05 Feb 2026 23:12:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:1b20d0583f0333315348ea321a9a2414adf640eded28a70f84ed2fd4bd564271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3513220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ba7ff46998f53254991cfc6e29a7a7e819d7a78371298c84c3909f594e3a6`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd3036ecb5b5912a7bf5e959fbcf6949977d95185e394621d290f86d3b690a`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 3.5 MB (3486638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883e3cc19bcf0d3b81736a31c83c87392e8c130bf3648efaf240813b81f6c6db`  
		Last Modified: Thu, 05 Feb 2026 23:12:38 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:ba12ddb9768ed2756bb1d6b366e9424b4f89e2dfe479f1d7dd14a22b2a2f2041
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
$ docker pull ghost@sha256:1e4ee020e2a934cad839a7d78db45e915e8bb1ed4253b4a84acaadb4ddcb09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230480850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7516d3b1fbdbe835b1598daf3407ef606b63ae076232f91b426d0a2e07878847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:24 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:49:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:49:59 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:59 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:07:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:07:51 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:07:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:08:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:08:05 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:10:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:10:10 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:10:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:10:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:10:10 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:10:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ed64e7a008278cf34abf2026687487ede329b69e00128254149c521a28114`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a949cc78c135e4c7782f1eaa160c32b8909ed92c92e1d93af305e90ab8836`  
		Last Modified: Tue, 03 Feb 2026 02:50:15 GMT  
		Size: 49.5 MB (49472749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ba10a6202898fef83665f67851cc21b882feb71575601c31d5a731ab99179`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.7 MB (1712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab0aa7de645eeb66edcb219492429b32ba52d15b200e2a1a825abcb272113`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5eb1bed0055cf75066e50262fdb530718ee91df609f7a791b92d9f1b10deb`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 1.2 MB (1247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf915476bf555500acac04af1fdbb6bbb93fde0a95dba0d03a71553655e051cc`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 12.1 MB (12138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045489bb500662becd60d2c79a2acf15a89b3f822d3d5dbb92cda7c99ddd6c8`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 137.7 MB (137676693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66195888a61484027b0b19be69c25ace3ed912bd9fa0fe1ca2091f7dbbbb3e11`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:5c459db002cfb1f85dd23f2ab5b633b13bbb61e773d3a97e6c826e3afb6f10d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496e6dad0f1404ce1c7a1657af4f7cd26e8bd428182d82c1adeca2dd714be7`

```dockerfile
```

-	Layers:
	-	`sha256:a10c25a5b9aa9089fe5029e67c9f2c995510730685088ad5dfb660036571b0cd`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 5.7 MB (5699133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86697e9f11b2029566321d9ee9bec2516aae7b69a157b255bb5f2af5d4eebe63`  
		Last Modified: Thu, 05 Feb 2026 23:10:46 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:a49d8a353df3338fea0ffabad82b0403eb01c93470591af1aec4e42b70a63293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221943581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa6d34fcfba908f25fa49bdd745817b0bde60512c26b735c5ce36426cf3ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:42:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:42:48 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:48 GMT
CMD ["node"]
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:43:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:43:36 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 22:43:36 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 22:43:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 22:43:50 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 22:46:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 22:46:40 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:46:40 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 22:46:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c1a837a11cbb768ebfcbb18795e80c0fbe6fc38f4365babd0fa29f57b958d`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972722eaf9eaf09e0a0b7092f02ff8da1b48cc469f55ce8a1b4c2e2b42b5f7b`  
		Last Modified: Tue, 03 Feb 2026 03:43:03 GMT  
		Size: 44.2 MB (44209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b36daa3a37ccb27912d51fc65b68e9e25ae53527872ad333984623cfc0b87`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 1.7 MB (1712843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164f20af1eab11f018853b1c5bac3d94bb9a23954d21c3cad6fd68da5f74c19`  
		Last Modified: Tue, 03 Feb 2026 03:43:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ebb6493d84f2290dcb37a3e2c80c0e1da0a8a1c166cde3dd94eb8213d439c`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 1.2 MB (1214403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2fe9f2912e55c8dbc333dbe8bff22394b1ec7c27a51c9dce7a8c84131b5b3`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 12.1 MB (12131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67941d4a8e2cd25c53811fb2410216f725a094b44880a6373c8e7a74b979faa9`  
		Last Modified: Thu, 05 Feb 2026 22:47:20 GMT  
		Size: 138.7 MB (138736878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a35c573e28c2906c0cc5e8c61627db2d02bd9b10f4380571e5ec6de309c68a`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:f759c1dd19745df891cf05e66aaa7d67126faf506a3ddce249dfaf326fe9fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c83ca393a017ad829978249d8141fba4aa4ce9e7eeb1bbbb5a84e9654c7c44`

```dockerfile
```

-	Layers:
	-	`sha256:5f22026a77aeb9ca973407ba78962ef4659fa5e90a2bae572a6cfee6dc2b9b64`  
		Last Modified: Thu, 05 Feb 2026 22:47:17 GMT  
		Size: 5.7 MB (5701930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fceaf910cc27688794651a72ac64a0f15a870dc0dd138b61219c6b9077c9b`  
		Last Modified: Thu, 05 Feb 2026 22:47:16 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b29cc92d4e08072f80d122c06a528de7e97cd53505df174444638071782d6263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230543203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4207414d184a6d41a6eb272edb22b6ff645c33c9c954fdcef1574680df7d3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 02:52:21 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:21 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 02:52:33 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:52:33 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:09:14 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:09:25 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:09:25 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:11:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:11:47 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:11:47 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:11:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f385b5be8d035c3eded4c8227017d8cf3dad57076037bced08574e1f9b7074`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950eedb50a8980370f35ad7c50613da2eec6b04d6ff2620e1f03c68feffc5f7`  
		Last Modified: Tue, 03 Feb 2026 02:52:49 GMT  
		Size: 49.6 MB (49611054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866a3bdc7ffd8790bbd9b876351d9c0e5a4149f9ba5066f490568e1f5b85`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 1.7 MB (1712647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68688986cf06d914cbbfdd366552e3f50d071aaf6970294be683a9555fefa12f`  
		Last Modified: Tue, 03 Feb 2026 02:52:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24942139376867ea27e692f69314b02698e0aab7ca58681960b3358306a3950f`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 1.2 MB (1201531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac77d82a52de96ab6b51e36dd0f42377a7ea4a9d60ac73848a144597206c3420`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 12.1 MB (12138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8edb0aed5966442ecb17e710c00bb579fe75834978e92793b01d9b585052dc9`  
		Last Modified: Thu, 05 Feb 2026 23:12:28 GMT  
		Size: 137.8 MB (137767270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5f357229e4184e3ac461769570c7b6132e81fb1f420afc3a43d2135647a64`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:132acae3398c326b91eb810df69f48d36f5d9a8a9dfdeb3027e8d53808955330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c4776f733b8a428f45b0f2ee04ece3fcf1b77910829352bd63a7418f139dcc`

```dockerfile
```

-	Layers:
	-	`sha256:58bb3d45964e16801f92103a3d614c872b44ea5232a2a6c0bc8997984282ce20`  
		Last Modified: Thu, 05 Feb 2026 23:12:26 GMT  
		Size: 5.7 MB (5699484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6d9e7d0017894ef4750ac8c5b968e583d02232831326262633a6de388c6899`  
		Last Modified: Thu, 05 Feb 2026 23:12:25 GMT  
		Size: 26.5 KB (26528 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:a4ca40a1034d78eecc852ee50df888ba5c94d968b1ef825ef3f948713258941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232443050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f967001b7833d135b156402a027c958f32ae2ffa1b7f335ca7034a0bc810b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:51:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV NODE_VERSION=22.22.0
# Tue, 03 Feb 2026 03:51:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:46 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Feb 2026 03:51:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:58 GMT
CMD ["node"]
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:10:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:10:54 GMT
ENV NODE_ENV=production
# Thu, 05 Feb 2026 23:10:54 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 05 Feb 2026 23:11:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 05 Feb 2026 23:11:21 GMT
ENV GHOST_VERSION=6.17.0
# Thu, 05 Feb 2026 23:13:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
WORKDIR /var/lib/ghost
# Thu, 05 Feb 2026 23:13:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 05 Feb 2026 23:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:13:32 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 05 Feb 2026 23:13:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff4659e19e18682ce4ffd0d04a37c9c50fd8b384588cfa41153cf28ea55b14`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc095ce2a117ed04609004c8a1ec2355194f08547e51f1a6332986648d16b5c9`  
		Last Modified: Tue, 03 Feb 2026 03:52:22 GMT  
		Size: 49.7 MB (49677683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454ce9ff6a9ef4895d3d231ce22d7acd14211502f7535f5b6204544009241ea`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 1.7 MB (1712697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa2bcc7e00f99a4cde53e93d9ae779755c8f7fab52c96eacf56da267feb674`  
		Last Modified: Tue, 03 Feb 2026 03:52:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119cf75e1aded1765c26a73ef5a0171addb2f5643ffed95b4cb914e3fed7748`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 1.2 MB (1221363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3838e52189d7bbd13434623a90cd85c71f7d4fe017571570a489847a0d8bf`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 12.1 MB (12146243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d11a0d42eaf34b4ebec47af9908bbb7dc4b2bb3c15d6b3142ec6a64da0b48`  
		Last Modified: Thu, 05 Feb 2026 23:14:29 GMT  
		Size: 140.8 MB (140796351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9180991791dec9c3e88b0768cf2e4b99245ed9589f0f973afbb146bd1cc4e`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:63a2fc9c9ed16d8481ad6f68257c23993d45602b9a4b151e6ad1d1191818d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f769b1d19c29cb2c6c3ee7dca73835deb7db64997a1f7ccd88d01555d42e3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c5788afe97446765e249392c9329677f4f93ace0618a9fedf5c78a51f9df5`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 5.7 MB (5692958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6847c996400ae5565aad75597ae392100cd1663f5e32a58daeafae8ce2038c50`  
		Last Modified: Thu, 05 Feb 2026 23:14:26 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

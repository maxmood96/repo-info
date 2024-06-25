## `node:lts-slim`

```console
$ docker pull node@sha256:9d37f39e4862726b0013dcf157a428015ef871dbbc00770b0547f1d8b67cc8cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:lts-slim` - linux; amd64

```console
$ docker pull node@sha256:fb1ba95488bd8839f5d28ac0f6372ded3121d68850d0a0835d848cdc361efe17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71430073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba03f9153c80226a3c758662f652fb081273dc4752215a8af25da659dda17143`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 14:33:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c71ec15baa93cc6a5b6b4ba149ceea36c10286a285171338df52794bef4ab`  
		Last Modified: Mon, 24 Jun 2024 21:54:45 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eee747f3db87aa901200402d1b4bf55ea73e029fe18dc382888f75680e9a96`  
		Last Modified: Mon, 24 Jun 2024 21:54:45 GMT  
		Size: 40.6 MB (40560835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522d2fdafee1e21f8d63f31fbc2b73692142661680f6382f4fc352cde58fcd79`  
		Last Modified: Mon, 24 Jun 2024 21:54:45 GMT  
		Size: 1.7 MB (1715040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4678a4e586010ca9c8949e8dc330ca5361dbd5a0fe255adc416f891477439aad`  
		Last Modified: Mon, 24 Jun 2024 21:54:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-slim` - unknown; unknown

```console
$ docker pull node@sha256:78bde8e57dfa604d6bc9a9741840dfbfab9cf56b7f05997c9ff222cb4803a6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0bb21db08e7a23762f5ddb889668e2f4c9bea0f10a6d1f10ce9583a6e31d3b`

```dockerfile
```

-	Layers:
	-	`sha256:5c57a59b99d970717db6a081dc4771f2f5e87c022ae86d0f384ba2c7f0622a17`  
		Last Modified: Mon, 24 Jun 2024 21:54:45 GMT  
		Size: 2.5 MB (2470977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee52c6b91157dc606ab7c31da6a7e1a4fb045be7ec78dc85dd15bef0d61c982`  
		Last Modified: Mon, 24 Jun 2024 21:54:45 GMT  
		Size: 27.5 KB (27468 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:2938c10e2ce0c0d1abd4fa082e9e7cd8a98b96c34f2cc83d19438b0689c80c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63147029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754893cd43944f8567a5a55fe2d40a5568ee73842726c9940d25d319b1c0b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 28 May 2024 18:47:58 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Tue, 28 May 2024 18:47:58 GMT
CMD ["bash"]
# Tue, 28 May 2024 18:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV NODE_VERSION=20.14.0
# Tue, 28 May 2024 18:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV YARN_VERSION=1.22.22
# Tue, 28 May 2024 18:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 28 May 2024 18:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 May 2024 18:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a179a90e0f9aa4d42977b6fd530865f1dd5e397e772aef64662dece3387f1801`  
		Last Modified: Fri, 21 Jun 2024 08:15:22 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804c868d3fa4eb50c1eeb838e086a3202555932d00625fc9e7a68b5324c33fac`  
		Last Modified: Fri, 21 Jun 2024 10:05:04 GMT  
		Size: 36.7 MB (36687581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04da8d2811ba854e582abb69041d4bf35a29e027fc435b19803cd61186a9087e`  
		Last Modified: Fri, 21 Jun 2024 10:05:03 GMT  
		Size: 1.7 MB (1715465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e3c7a3895aed4e92b5905c94985bf9fb1f4154e6e4afd9d2e058208d257fe9`  
		Last Modified: Fri, 21 Jun 2024 10:05:03 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-slim` - unknown; unknown

```console
$ docker pull node@sha256:02eb6275737d6333c04a48094587f41772f0724389f395718d587b5714212484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e021a0ab2b1264b34c27f851e43014493cada63865ebf6b49ce5c2ec263ee839`

```dockerfile
```

-	Layers:
	-	`sha256:3c33750c633424ef7b5da7e6d5fb895ae90188cd2ae2cb7f4428a6c78c7679c5`  
		Last Modified: Fri, 21 Jun 2024 10:05:03 GMT  
		Size: 2.5 MB (2476245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08abf16ffde4d89ac8f72abd6c4553de1bdc7a9f62d987c86486580fd2d4d9cc`  
		Last Modified: Fri, 21 Jun 2024 10:05:03 GMT  
		Size: 27.6 KB (27612 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0792cb19ab49b5b62148fd2843273986cbd601e3090c24747b52b2360888b542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71427043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4078eabcc6d97627ae346adc1e169d631b5d30e72deafcc8476be6c090a4b61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 14:33:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b278c63f43755efa363f5f0b25a4cff20fa1b3e26b0fb85639672bc1e2adfad3`  
		Last Modified: Fri, 21 Jun 2024 08:42:10 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116df4e2b183ee738b85edfc7d0b11c093bbc2127295a3ba9c4d041dd7e756ba`  
		Last Modified: Mon, 24 Jun 2024 22:47:37 GMT  
		Size: 40.5 MB (40528431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd24b0b1f35f9f0bf0621064e397405cf1d6551f8e3171c803bedd516f87996`  
		Last Modified: Mon, 24 Jun 2024 22:47:36 GMT  
		Size: 1.7 MB (1715177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9ff5234c1ad24a6b54351ee9efc74c86da190ca1774f9c228cf4a11e06e5fe`  
		Last Modified: Mon, 24 Jun 2024 22:47:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-slim` - unknown; unknown

```console
$ docker pull node@sha256:9846d060ad5f43039dd7ef8007e2efcc7f8199b0b4c40ffc5924d52e3796a5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ea65c3be67056a862085e1b9ed7afbbb915698c39cf6e913774739a70bafaa`

```dockerfile
```

-	Layers:
	-	`sha256:966f777672c057cd504330a8309f1120f652e9580973fac880ae1753987163e8`  
		Last Modified: Mon, 24 Jun 2024 22:47:36 GMT  
		Size: 2.5 MB (2471299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01981cf626c13946a3b02d8e84e946c7fb877cd005149c80f7710bdfc20ede66`  
		Last Modified: Mon, 24 Jun 2024 22:47:35 GMT  
		Size: 27.8 KB (27849 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-slim` - linux; ppc64le

```console
$ docker pull node@sha256:9ccb698f45e0618be0bb8cad3ea4b394c40a50d359028df7571065fd9a9c64a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77893703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8fcd89679edba24c69a30599a0249822f30577de8f3946ee7590a2b392611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:04 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Thu, 13 Jun 2024 01:17:06 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 14:33:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a460818ffa12a10c3daeaca8a19efbe428554a770671999655aaae923f821aa1`  
		Last Modified: Fri, 21 Jun 2024 03:41:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4385a39dbd4ae03ee24e44e645997a5996e3aa339dc26820dbdfd1f36f26bf56`  
		Last Modified: Mon, 24 Jun 2024 22:30:28 GMT  
		Size: 43.0 MB (43033445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14df6288cbfad243e9b4f3930378310201190de32725159f3b2078b2ccbf5bb6`  
		Last Modified: Mon, 24 Jun 2024 22:30:27 GMT  
		Size: 1.7 MB (1715299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136cdf547293e9e2acdf6185b00a50041b1350c652d532da0a9979c4303c9dd`  
		Last Modified: Mon, 24 Jun 2024 22:30:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-slim` - unknown; unknown

```console
$ docker pull node@sha256:2290b800e285b24fef67bdf828a0c73a6d67eca21d957f67dc8a8a1df8655283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c214f1a850a4a436b34cca4f1a444ce0f001c208c36da936ab1466a1957d4d`

```dockerfile
```

-	Layers:
	-	`sha256:19f89f3da730ea477b59a74953cef09ef7d015e6888dd142c2b0da56587896e8`  
		Last Modified: Mon, 24 Jun 2024 22:30:27 GMT  
		Size: 2.5 MB (2475270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9fc2d13e3a3a5d2d1fa4b78ea9755ab2ad448d34e5c93fd3b9a74cebae049a`  
		Last Modified: Mon, 24 Jun 2024 22:30:26 GMT  
		Size: 27.5 KB (27546 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-slim` - linux; s390x

```console
$ docker pull node@sha256:3579c74f332b19df9f616082da8f071bdeff963aaac8dc5b61f408739c66cfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70023080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba6f512a12f0d8bee279903915e2ac961ec0d3a019bd909bdc989f38f71ff03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 28 May 2024 18:47:58 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Tue, 28 May 2024 18:47:58 GMT
CMD ["bash"]
# Tue, 28 May 2024 18:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV NODE_VERSION=20.14.0
# Tue, 28 May 2024 18:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV YARN_VERSION=1.22.22
# Tue, 28 May 2024 18:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 28 May 2024 18:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 May 2024 18:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd23c88b2ce35235981c879ce1ea97faceb78be47203b68eff04d9511d9abcb9`  
		Last Modified: Fri, 21 Jun 2024 09:38:06 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0f110fe3dd72a8613439c44b6c1cb8256183dd59c875aef53c74c9edd5f6be`  
		Last Modified: Fri, 21 Jun 2024 11:11:28 GMT  
		Size: 40.8 MB (40791708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca97cc8f8932a42a4f2141d6c87c99fdb6463b5a9ef40c09d92abeffcb46f41a`  
		Last Modified: Fri, 21 Jun 2024 11:11:27 GMT  
		Size: 1.7 MB (1715146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d4d8323a9a01edc46b4a3f06a21c9da1673eb1f00f544922b2a2d2edb5153b`  
		Last Modified: Fri, 21 Jun 2024 11:11:27 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-slim` - unknown; unknown

```console
$ docker pull node@sha256:e5c20f5dce9dd0aea9787b0015e336212781d4dd255b7418227b1f22c44f2d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66019a8af95df98104a0d57bab87f32b762685cc4a8a84f12a128b11badb4eaf`

```dockerfile
```

-	Layers:
	-	`sha256:c5f3d7dc6c491b256d1e0d2bc7ce52b3363f252ac13729eec05bd6af21ac48ad`  
		Last Modified: Fri, 21 Jun 2024 11:11:28 GMT  
		Size: 2.5 MB (2470814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5422ed25df43913315757a8076391aad1a775f75ad742c3e455966953cf5da9`  
		Last Modified: Fri, 21 Jun 2024 11:11:27 GMT  
		Size: 27.5 KB (27468 bytes)  
		MIME: application/vnd.in-toto+json

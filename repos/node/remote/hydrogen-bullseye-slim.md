## `node:hydrogen-bullseye-slim`

```console
$ docker pull node@sha256:ea50209837694d0f402478d07defc2a406a465f2aa882fc8d01caa12fdd572e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:hydrogen-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:c9260b0a6d8ed81c3636de4a3baa248729540d631c6d9355513c4538fe9ab4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70266120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe6041aa05da08cd6da7d8250c42f0aab31d3e8fa72b9ced92bf17133d18604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 27 Mar 2025 14:23:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV NODE_VERSION=18.20.8
# Thu, 27 Mar 2025 14:23:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 27 Mar 2025 14:23:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 14:23:08 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fdab1ca6f18e46abf4b803ec42f0c44f970ffb49518b6fa697ad496182c202`  
		Last Modified: Thu, 27 Mar 2025 14:33:36 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c83fdbeca84c2f292b140b0e2030e7a65ea5cff47bb0b2a8bf37725e893f26`  
		Last Modified: Thu, 27 Mar 2025 14:33:38 GMT  
		Size: 38.3 MB (38271753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b367cca9319236980a4a3432e49a6272327dbf9cc35cbbb16f7d3aa8b458d`  
		Last Modified: Thu, 27 Mar 2025 14:33:37 GMT  
		Size: 1.7 MB (1736008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856bbee9d77bbbb912106c882c1770f207b15841f2d7096e37590f09fe59bb84`  
		Last Modified: Thu, 27 Mar 2025 14:33:37 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:bc3f4c82d98b8934fb47cbca3945341858d1fdedec04de3cef8f8d3501f042f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2d8236a45e6ab188005bd94e34037677e0313bfec2e509a8f3dbc76bfe7cea`

```dockerfile
```

-	Layers:
	-	`sha256:9667d4b62471bcb1558a5946e5d3725d6964cef58d6dc61de152ed537bde537e`  
		Last Modified: Thu, 27 Mar 2025 14:33:37 GMT  
		Size: 2.9 MB (2850047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6249cf20d24c2b40db9a773aabc24ff5fd573788def8ba7f8c491615f2927459`  
		Last Modified: Thu, 27 Mar 2025 14:33:36 GMT  
		Size: 25.2 KB (25240 bytes)  
		MIME: application/vnd.in-toto+json

### `node:hydrogen-bullseye-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:e05642398d05da3c737cec85a11a599dad4863d11dc4f8e55074125defaeb733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62210210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1ff27809a9ca88b080bd3f81c4d16f0962b214b3f68f1ee4f9ba6c83deb614`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Feb 2025 11:20:37 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2627a71e88bf658ab90653bc463b3684725a0683a10cfc9d275f2572a246f349`  
		Last Modified: Tue, 18 Mar 2025 04:49:14 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeb2ede6cac092bb12dcf15a44f3ed88b2bed7bf53955e584d8b65a1083e1c9`  
		Last Modified: Tue, 18 Mar 2025 04:49:16 GMT  
		Size: 34.9 MB (34934239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464afa9e7434c0d4e24ec443b383d25056c86ce23d5b45b6035b9c21ccd25775`  
		Last Modified: Tue, 18 Mar 2025 04:49:15 GMT  
		Size: 1.7 MB (1736123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8840e11687d62d1dddbd45807d90cf142b00f5b6c63fc48f61081db7a33100e9`  
		Last Modified: Tue, 18 Mar 2025 04:49:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:7e338e072dbe2f6169d8ce1aa7fb0212c6288cc67444bc8b7e542a5f33dc64d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a25eb3cb2756d740663c3a6925f4e64d8ea44df06533bb390a3f6fab3ee2b2`

```dockerfile
```

-	Layers:
	-	`sha256:474c7dc0af12b87246b4847308c0981b2d8331433948e3f8b005f6e14cac075b`  
		Last Modified: Tue, 18 Mar 2025 04:49:15 GMT  
		Size: 2.9 MB (2855533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d32400145d9d1acb516e5bc043772b6a3e6c84a4e4b633d5fbd1dfd5818c2780`  
		Last Modified: Tue, 18 Mar 2025 04:49:14 GMT  
		Size: 25.3 KB (25342 bytes)  
		MIME: application/vnd.in-toto+json

### `node:hydrogen-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:f5b68fe8a5d3698d646945c8f5c6385b9c93ab99034c362d3f451b750058130b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68816716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0577c5124ef63e126774dfee26cde5cf19a104356326a4cbd2d27e4c5bfd7a77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Feb 2025 11:20:37 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 20 Feb 2025 11:20:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV NODE_VERSION=18.20.7
# Thu, 20 Feb 2025 11:20:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENV YARN_VERSION=1.22.22
# Thu, 20 Feb 2025 11:20:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 11:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 11:20:37 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879d958352a1ab434cde018ab80b5366c27fe54ba8c63b35d2d39d39feddc099`  
		Last Modified: Tue, 18 Mar 2025 03:19:47 GMT  
		Size: 4.1 KB (4077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd4027074d61ea68710bd59ae1da17fc1316ad736388fc14f635e6aedc84cc0`  
		Last Modified: Tue, 18 Mar 2025 03:19:49 GMT  
		Size: 38.3 MB (38330389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20eee0570ff36ae473d9575503bad63a86efff601e78a1d7a0b8b7e872a06d`  
		Last Modified: Tue, 18 Mar 2025 03:19:48 GMT  
		Size: 1.7 MB (1735880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d53d8dacaaa28e0524045f6a8a26607229ff23318937bcf58e9f58e0de3d1e`  
		Last Modified: Tue, 18 Mar 2025 03:19:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:4668cbc8ac88c548e428470744ac2251cfe17a315b1a05bf3494ddd349295725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2116579bd4480387f6607e0a7cd492f153b284f5ee6e9c7f2537b2f4e3c95aed`

```dockerfile
```

-	Layers:
	-	`sha256:3cf8b74be09e0c515c18e01887fa99868f55f87566eaf25ad54b39462c80fc87`  
		Last Modified: Tue, 18 Mar 2025 03:19:48 GMT  
		Size: 2.9 MB (2850298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa8812d03f21ab59b5f7d6b3c8591457d5d637e43c821d2d85d05d3294cc7e`  
		Last Modified: Tue, 18 Mar 2025 03:19:47 GMT  
		Size: 25.4 KB (25374 bytes)  
		MIME: application/vnd.in-toto+json

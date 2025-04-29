## `node:bullseye-slim`

```console
$ docker pull node@sha256:6cab979d4528a00f8842d4bf29104b11e9203b3f2b4e52e83c1eccc4d064d113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:98fd895037b414c00f8bc24c76101563c1ac6054ac6d904c93af0b0ab2581f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82100064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272829a91c44620b75d2ee81ed911b309a3740547234698aa6965bbd1de9ae13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 01 Apr 2025 16:05:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedd53ffb22128b078bb1c7bef6aefa410caff8dc1172ca8817c21d816ab7fb4`  
		Last Modified: Mon, 28 Apr 2025 21:57:41 GMT  
		Size: 4.1 KB (4065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fd71384e2b52435858ad5ec9c82d238dd5944a3a9265e6fedcab228c5f658b`  
		Last Modified: Mon, 28 Apr 2025 21:57:42 GMT  
		Size: 50.1 MB (50104888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cdb9333ee496daa7b4041038fa28ccc72a72eddfeb3e1a8a0ac8341fa336bd`  
		Last Modified: Mon, 28 Apr 2025 21:57:41 GMT  
		Size: 1.7 MB (1736059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3c29ec8f6b46cf912d724551b49fe3ebdf640f4f7468d82b7a095457629edd`  
		Last Modified: Mon, 28 Apr 2025 21:57:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:834eb3afd574a341317e53afe7776c3d6f5e8a12f77ce8ac22d9fff321793b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2895064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136e84fb6327889f205545e2440e0ccc2514232f07946b35734ee03d595b5aad`

```dockerfile
```

-	Layers:
	-	`sha256:a3d62d769d42f3bf504d6fe2abd0cef0e6c4a192516394403a61244be82ed23b`  
		Last Modified: Mon, 28 Apr 2025 21:57:41 GMT  
		Size: 2.9 MB (2869519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5df669bafd973d70bd080723aabfa809204cf642fa4daa43b7042111e95a1cc`  
		Last Modified: Mon, 28 Apr 2025 21:57:41 GMT  
		Size: 25.5 KB (25545 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:3594732fc63f9443ee3af12db6b8100ad9c08df52e5bdef5cb84168e3ca9812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80075438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dbaf0adc3eb24a8f515f4d07d649c79e9424716f1ed9cb211265542ce38382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 01 Apr 2025 16:05:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eb6d9f63c44e8a57c34416961078ad799315c7539ae27e4e72197a09acb9d`  
		Last Modified: Tue, 08 Apr 2025 06:38:19 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bdc508eb392e68c6a9a1ce7e5e18397194ba25d6633176ef0471f2cc3a557c`  
		Last Modified: Tue, 08 Apr 2025 06:38:21 GMT  
		Size: 49.6 MB (49585412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ef90e9d2b2c1e23899545481ef853e41143fbfccf5d6d347df2cf957aa02fb`  
		Last Modified: Tue, 08 Apr 2025 06:38:20 GMT  
		Size: 1.7 MB (1736009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159ebf7e790c1f81976d2b1ae19e1e7500a2403dc651e71c706a042c7b4caa10`  
		Last Modified: Tue, 08 Apr 2025 06:38:20 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:366c4cb0d5e927b0537b2e16ad483c61436328694d8069a7d2aa9a20f256ec30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2895419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf62441e47a99fca372aac3d8c44e0c719aa123449ea308d252eb7e809608c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb9bb3187ebd86f394fbf6c81cc02c890b15f86ce481b8076b0ba1c511951aec`  
		Last Modified: Tue, 08 Apr 2025 06:38:20 GMT  
		Size: 2.9 MB (2869728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f86ebe792e5de74f8cb8ffc4e695c1c6fb96eeef91509e752966228c7cee6c`  
		Last Modified: Tue, 08 Apr 2025 06:38:19 GMT  
		Size: 25.7 KB (25691 bytes)  
		MIME: application/vnd.in-toto+json
